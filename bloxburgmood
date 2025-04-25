local Players = cloneref(game:GetService("Players")) :: Players
local RunService = cloneref(game:GetService("RunService")) :: RunService
local LocalPlayer = Players.LocalPlayer

local PerfectMood = {
	Config = {
		DesiredMood = "Happy",
		DesiredValue = 100,
		UpdateFrequency = 3,
		Threshold = 5,
	},
	State = {
		CachedMoodStats = nil,
		CachedMoodModule = nil,
		IsInitialized = false,
	},
	MoodTypes = {"Happy", "Energy", "Hygiene", "Hunger", "Fun"},
}

function PerfectMood:GetMoodModule()
	if self.State.CachedMoodModule then 
		return self.State.CachedMoodModule 
	end
	
	for _, module in next, getgc(true) do
		if type(module) == "table" and rawget(module, "SetMood") and rawget(module, "GetMood") then
			self.State.CachedMoodModule = module
			return module
		end
	end
	
	return nil
end

function PerfectMood:GetMoodStats()
	if self.State.CachedMoodStats then 
		if #self.State.CachedMoodStats > 0 and self.State.CachedMoodStats[1].Parent ~= nil then
			return self.State.CachedMoodStats
		end
	end
	
	local moodModule = self:GetMoodModule()
	if moodModule and moodModule.Modules and moodModule.Modules.ClientStats then
		local _, moodData = moodModule.Modules.ClientStats:Get("MoodData")
		if moodData then
			self.State.CachedMoodStats = moodData:GetChildren()
			return self.State.CachedMoodStats
		end
	end
	
	for _, instance in next, LocalPlayer:GetDescendants() do
		if instance.Name == "MoodData" and #instance:GetChildren() > 0 then
			self.State.CachedMoodStats = instance:GetChildren()
			return self.State.CachedMoodStats
		end
	end
	
	return {}
end

function PerfectMood:NeedsUpdate(moodName: string): boolean
	local moodStats = self:GetMoodStats()
	
	for _, stat in next, moodStats do
		if stat.Name == moodName then
			for _, propName in next, {"Value", "value"} do
				if stat[propName] ~= nil then
					return (self.Config.DesiredValue - stat[propName]) > self.Config.Threshold
				end
			end
		end
	end
	
	return false
end

function PerfectMood:SetMoodValueIfNeeded(moodName: string): boolean
	if not self:NeedsUpdate(moodName) then 
		return false 
	end
	
	local moodStats = self:GetMoodStats()
	for _, stat in next, moodStats do
		if stat.Name == moodName then
			for _, propName in next, {"Value", "value"} do
				if stat[propName] ~= nil then
					stat[propName] = self.Config.DesiredValue
					return true
				end
			end
		end
	end
	
	return false
end

function PerfectMood:Initialize()
	if self.State.IsInitialized then 
		return 
	end
	
	local moodModule = self:GetMoodModule()
	if not moodModule then
		warn("PerfectMood: Couldn't find mood module!")
		return
	end
	
	for _, mood in next, self.MoodTypes do
		local moodStats = self:GetMoodStats()
		for _, stat in next, moodStats do
			if stat.Name == mood and stat:FindFirstChild("Rate") then
				local rateValue = stat.Rate
				
				local oldSet
				oldSet = hookmetamethod(rateValue, "__newindex", newcclosure(function(self, index, value)
					if self == rateValue and index == "Value" and value < 0 then
						return oldSet(self, index, 0)
					end
					return oldSet(self, index, value)
				end))
			end
		end
	end
	
	self.State.IsInitialized = true
	print("PerfectMood: Controller initialized")
end

function PerfectMood:UpdateMoods()
	local updated = false
	
	for _, mood in next, self.MoodTypes do
		if self:SetMoodValueIfNeeded(mood) then
			updated = true
		end
	end
	
	if updated then
		local moodModule = self:GetMoodModule()
		if moodModule and moodModule.SetMood then
			pcall(function()
				moodModule:SetMood(self.Config.DesiredMood)
			end)
		end
	end
end

function PerfectMood:Start()
	self:Initialize()
	
	spawn(function()
		while true do
			local success, err = pcall(function() 
				self:UpdateMoods() 
			end)
			
			if not success then
				warn("PerfectMood: Error in mood controller:", err)
			end
			
			wait(self.Config.UpdateFrequency)
		end
	end)
	
	print("PerfectMood: Controller active with update frequency: " .. self.Config.UpdateFrequency .. "s")
end

PerfectMood:Start()

return PerfectMood
