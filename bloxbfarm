do
BloxburgGUI = Instance.new("ScreenGui")
syn.protect_gui(BloxburgGUI)
Main = Instance.new("Frame")
TextLabel = Instance.new("TextLabel")
Main_2 = Instance.new("Frame")
CashierBloxyBurgersLabel = Instance.new("TextLabel")
UIListLayout = Instance.new("UIListLayout")
killguilabel = Instance.new("TextLabel")
hideguilabel = Instance.new("TextLabel")
HairdresserLabel = Instance.new("TextLabel")
UICorner = Instance.new("UICorner")

--Properties:

BloxburgGUI.Name = "BloxburgGUI"
BloxburgGUI.Parent = game.CoreGui
BloxburgGUI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = BloxburgGUI
Main.BackgroundColor3 = Color3.fromRGB(29, 29, 29)
Main.Position = UDim2.new(0.802118957, 0, 0.269811392, 0)
Main.Size = UDim2.new(0, 182, 0, 201)

TextLabel.Parent = Main
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(0, 0, 0.022580646, 0)
TextLabel.Size = UDim2.new(0, 182, 0, 41)
TextLabel.Font = Enum.Font.Ubuntu
TextLabel.Text = "Bloxburg GUI"
TextLabel.TextColor3 = Color3.fromRGB(128, 255, 0)
TextLabel.TextSize = 18.000

Main_2.Name = "Main"
Main_2.Parent = Main
Main_2.BackgroundColor3 = Color3.fromRGB(21, 21, 21)
Main_2.BackgroundTransparency = 0.990
Main_2.LayoutOrder = 1
Main_2.Position = UDim2.new(0, 0, 0.228668138, 0)
Main_2.Size = UDim2.new(0, 184, 0, 155)

CashierBloxyBurgersLabel.Name = "CashierBloxyBurgers"
CashierBloxyBurgersLabel.Parent = Main_2
CashierBloxyBurgersLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CashierBloxyBurgersLabel.BackgroundTransparency = 1.000
CashierBloxyBurgersLabel.Position = UDim2.new(0, 0, 0.190045252, 0)
CashierBloxyBurgersLabel.Size = UDim2.new(0, 184, 0, 35)
CashierBloxyBurgersLabel.Font = Enum.Font.Ubuntu
CashierBloxyBurgersLabel.Text = "Bloxy Burgers Cashier (Q)"
CashierBloxyBurgersLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
CashierBloxyBurgersLabel.TextSize = 13.000

UIListLayout.Parent = Main_2
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder

killguilabel.Name = "killguilabel"
killguilabel.Parent = Main_2
killguilabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
killguilabel.BackgroundTransparency = 1.000
killguilabel.LayoutOrder = 100
killguilabel.Position = UDim2.new(0, 0, 0.153008223, 0)
killguilabel.Size = UDim2.new(0, 184, 0, 35)
killguilabel.Font = Enum.Font.Ubuntu
killguilabel.Text = "KILL GUI AND SCRIPTS (P)"
killguilabel.TextColor3 = Color3.fromRGB(255, 255, 255)
killguilabel.TextSize = 13.000

hideguilabel.Name = "hideguilabel"
hideguilabel.Parent = Main_2
hideguilabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
hideguilabel.BackgroundTransparency = 1.000
hideguilabel.LayoutOrder = 3
hideguilabel.Position = UDim2.new(0, 0, 0.190045252, 0)
hideguilabel.Rotation = 3.000
hideguilabel.Size = UDim2.new(0, 184, 0, 35)
hideguilabel.Font = Enum.Font.Ubuntu
hideguilabel.Text = "Hide Gui (RShift)"
hideguilabel.TextColor3 = Color3.fromRGB(255, 255, 255)
hideguilabel.TextSize = 13.000

HairdresserLabel.Name = "Hairdresser"
HairdresserLabel.Parent = Main_2
HairdresserLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
HairdresserLabel.BackgroundTransparency = 1.000
HairdresserLabel.Position = UDim2.new(0, 0, 0.190045252, 0)
HairdresserLabel.Size = UDim2.new(0, 184, 0, 35)
HairdresserLabel.Font = Enum.Font.Ubuntu
HairdresserLabel.Text = "Hairdresser (E)"
HairdresserLabel.TextColor3 = Color3.fromRGB(255, 0, 0)
HairdresserLabel.TextSize = 13.000

UICorner.CornerRadius = UDim.new(0.100000001, 8)
UICorner.Parent = Main
end

local a=game:GetService("UserInputService")local self={}local b=Main;local c=nil;local d=nil;local e=nil;local f=false;local function g(h)local i=h.Position-d;local j=UDim2.new(e.X.Scale,e.X.Offset+i.X,e.Y.Scale,e.Y.Offset+i.Y)b.Position=j;return j end;self.InputBegan=b.InputBegan:Connect(function(h)if kill then return end;if h.UserInputType==Enum.UserInputType.MouseButton1 or h.UserInputType==Enum.UserInputType.Touch then f=true;local k;k=h.Changed:Connect(function()if h.UserInputState==Enum.UserInputState.End and(self.Dragging or f)then self.Dragging=false;k:Disconnect()if self.DragEnded and not f then self.DragEnded()end;f=false end end)end end)self.InputChanged=b.InputChanged:Connect(function(h)if kill then return end;if h.UserInputType==Enum.UserInputType.MouseMovement or h.UserInputType==Enum.UserInputType.Touch then c=h end end)self.InputChanged2=a.InputChanged:Connect(function(h)if kill then return end;if f then f=false;if self.DragStarted then self.DragStarted()end;self.Dragging=true;d=h.Position;e=b.Position end;if h==c and self.Dragging then local j=g(h)if self.Dragged then self.Dragged(j)end end end)

local Colors = {Pink = -1,Green = -2,Blue = -3, Gray = 0,Blonde = 1,Brown = 2, Black = 3,Red = 4}
local Hairstyles = {Sideswept = -1,Curly = -2,Long = -3,Bun = -4,Afro = 0,Charming = 1,Combed = 2,Headband = 3,Pigtails = 4,Messy = 5}
local player = game:GetService"Players".LocalPlayer
local character = player.Character
local HairdresserWorkstations = game:GetService("Workspace").Environment.Locations.StylezHairStudio.HairdresserWorkstations
local CashierWorkstations = game:GetService("Workspace").Environment.Locations.BloxyBurgers.CashierWorkstations
local CAS = game:GetService("ContextActionService")

local CashierBloxyToggle = false
local CashierBloxyRun = false
local HairdresserToggle = false
local HairdresserRun = false

local function SetLabelActive(label,bool)
    if bool then
        label.TextColor3 = Color3.new(0,255,0)
    else
        label.TextColor3 = Color3.new(255,0,0)
    end
end

local function StopBloxyCashier() SetLabelActive(CashierBloxyBurgersLabel,false) CashierBloxyToggle = false CashierBloxyRun = false end
local function StopHairdresser() SetLabelActive(HairdresserLabel,false) HairdresserToggle = false HairdresserRun = false end

local function GetPlayerWorkstation(workstations)
    local closestworkstation = nil
    local distance = math.huge
    for _,part in ipairs(workstations:GetChildren()) do
        local partdistance = (part.PrimaryPart.Position - character.PrimaryPart.Position).Magnitude
        if partdistance < distance then
            closestworkstation = part
            distance = partdistance
        end
    end
    return closestworkstation
end

local function ClickButton(btn)
    local events = {"MouseButton1Up", "MouseButton1Down", "MouseButton1Click", "Activated"}
    for _,event in pairs(events) do
        for _,evnt in pairs(getconnections(btn[event])) do
            evnt:Fire()
        end
    end
end

local function CompleteBloxyCashierOrder()
    local workstation = GetPlayerWorkstation(CashierWorkstations)
    if not workstation then warn("[S] CashierBloxy: Could not find workstation") StopBloxyCashier() return false end
    local gui = workstation.OrderDisplay.DisplayMain.CashierGUI.Frame
    local customer = workstation.Occupied.Value
    if customer then
        local order = customer.Order
        local burger = order.Burger.Value
        local fries = order.Fries.Value
        local cola = order.Cola.Value
        if burger then ClickButton(gui:FindFirstChild(burger)) end
        if fries then ClickButton(gui.Fries) end
        if cola then ClickButton(gui.Cola) end
        wait(0.1)
        ClickButton(gui.Done)
        local done = Instance.new("BoolValue",workstation.Occupied.Value)
        done.Name = "Done"
    end
    return true
end

local function ToggleBloxyCashierAutoFarm()
    CashierBloxyToggle = not CashierBloxyToggle
    SetLabelActive(CashierBloxyBurgersLabel,CashierBloxyToggle)
    if CashierBloxyRun then return end
    CashierBloxyRun = true
    while CashierBloxyToggle do
        local workstation = GetPlayerWorkstation(CashierWorkstations) if not workstation then warn("[S] CashierBloxy: Could not find workstation") StopBloxyCashier() return end
        if workstation.Occupied.Value and workstation.Occupied.Value.Head:FindFirstChild("ChatBubble") and not workstation.Occupied.Value:FindFirstChild("Done") then
            if not CompleteBloxyCashierOrder() then StopBloxyCashier() return end
        end
        wait()
    end
    StopBloxyCashier()
end




local function CompleteHairdresserOrder()
    local workstation = GetPlayerWorkstation(HairdresserWorkstations)
    if not workstation then warn("[S] Hairdresser: Could not find workstation") StopHairdresser() return false end
    local customer = workstation.Occupied.Value
    if customer then
        local Style = customer.Order.Style.Value
        local Color = customer.Order.Color.Value
        if not Style or not Color then return false end
        
        local SurfaceGui = workstation.Mirror.HairdresserGUI.Frame
        local StyleGUI = SurfaceGui:FindFirstChild"Style"
        local ColorGUI = SurfaceGui:FindFirstChild"Color"
        local DoneGUI = SurfaceGui.Done
        
        local StyleChange = tonumber(Hairstyles[Style])
        local ColorChange = tonumber(Colors[Color])
        if StyleChange < 0 then
            while StyleChange < 0 do
                StyleChange = StyleChange+1
                ClickButton(StyleGUI.Back)
                wait(0.05)
            end
        elseif StyleChange > 0 then
            while StyleChange > 0 do
                StyleChange = StyleChange-1
                ClickButton(StyleGUI.Next)
                wait(0.05)
            end
        end
        if ColorChange < 0 then
            while ColorChange < 0 do
                ColorChange = ColorChange+1
                ClickButton(ColorGUI.Back)
                wait(0.05)
            end
        elseif ColorChange > 0 then
            while ColorChange > 0 do
                ColorChange = ColorChange-1
                ClickButton(ColorGUI.Next)
                wait(0.05)
            end
        end
        wait(0.1)
        ClickButton(DoneGUI)
            local done = Instance.new("BoolValue",workstation.Occupied.Value)
            done.Name = "Done"
    else return false end
    return true
end

local function ToggleHairdresserAutoFarm()
    HairdresserToggle = not HairdresserToggle
    SetLabelActive(HairdresserLabel,HairdresserToggle)
    if HairdresserRun then return end
    HairdresserRun = true
    while HairdresserToggle do
        local workstation = GetPlayerWorkstation(HairdresserWorkstations) if not workstation then warn("[S] Hairdresser: Could not find workstation") StopHairdresser() return end
        if workstation.Occupied.Value and workstation.Occupied.Value.Head:FindFirstChild("ChatBubble") and (not workstation.Occupied.Value:FindFirstChild("Done")) then
            if not CompleteHairdresserOrder() then StopHairdresser() return end
        end
        wait()
    end
    StopHairdresser()
end


CAS:BindAction("ToggleGUI",function(_,state,_) if state~=Enum.UserInputState.End then return end BloxburgGUI.Enabled = not BloxburgGUI.Enabled end,false,Enum.KeyCode.RightShift)
CAS:BindAction("ToggleBloxyCashierAutoFarm",function(_,state,_) if state~=Enum.UserInputState.End then ToggleBloxyCashierAutoFarm() end end,false,Enum.KeyCode.Q)
CAS:BindAction("ToggleHairdresserAutoFarm",function(_,state,_) if state~=Enum.UserInputState.End then ToggleHairdresserAutoFarm() end end,false,Enum.KeyCode.E)
CAS:BindAction("Kill",function() BloxburgGUI:Destroy() CAS:UnbindAction("Kill") CAS:UnbindAction("ToggleGUI") CAS:UnbindAction("ToggleHairdresserAutoFarm") CAS:UnbindAction("ToggleBloxyCashierAutoFarm") StopHairdresser() StopBloxyCashier() end,false,Enum.KeyCode.P) syn.protect_gui(BloxburgGUI)
