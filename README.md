-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local DeszK = Instance.new("Frame")
local Deszkv10 = Instance.new("TextLabel")
local REACH = Instance.new("TextButton")
local AIMLOCK = Instance.new("TextButton")
local SPEED = Instance.new("TextButton")
local TextBox = Instance.new("TextBox")
local ANIMACIONES = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

DeszK.Name = "DeszK"
DeszK.Parent = ScreenGui
DeszK.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
DeszK.BorderColor3 = Color3.fromRGB(27, 27, 27)
DeszK.Position = UDim2.new(0.0611664355, 0, 0.313662082, 0)
DeszK.Size = UDim2.new(0, 414, 0, 247)

Deszkv10.Name = "彡 DeszK v1.0"
Deszkv10.Parent = ScreenGui
Deszkv10.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
Deszkv10.Position = UDim2.new(0.061166428, 0, 0.315682292, 0)
Deszkv10.Size = UDim2.new(0, 414, 0, 50)
Deszkv10.Font = Enum.Font.SourceSans
Deszkv10.Text = "彡 DeszK v1.0"
Deszkv10.TextColor3 = Color3.fromRGB(0, 0, 0)
Deszkv10.TextSize = 35.000

REACH.Name = "REACH"
REACH.Parent = Deszkv10
REACH.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
REACH.BorderColor3 = Color3.fromRGB(0, 0, 0)
REACH.Position = UDim2.new(0, 0, 1, 0)
REACH.Size = UDim2.new(0, 120, 0, 34)
REACH.Font = Enum.Font.SourceSans
REACH.Text = "Reach [Solo Cuchillo]"
REACH.TextColor3 = Color3.fromRGB(0, 0, 0)
REACH.TextSize = 14.000
REACH.MouseButton1Down:connect(function()
	game.Players.LocalPlayer.Backpack["[Knife]"].Handle.Size = Vector3.new(100, 100, 100)
	game.Players.LocalPlayer.Backpack["[Knife]"].Handle.Size = Vector3.new(100, 100, 100)
end)

AIMLOCK.Name = "AIMLOCK"
AIMLOCK.Parent = Deszkv10
AIMLOCK.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
AIMLOCK.BorderColor3 = Color3.fromRGB(0, 0, 0)
AIMLOCK.Position = UDim2.new(0.289855063, 0, 1, 0)
AIMLOCK.Size = UDim2.new(0, 163, 0, 34)
AIMLOCK.Font = Enum.Font.SourceSans
AIMLOCK.Text = "Aimlock Toggle [Y]"
AIMLOCK.TextColor3 = Color3.fromRGB(0, 0, 0)
AIMLOCK.TextSize = 14.000
AIMLOCK.MouseButton1Down:connect(function()
	getgenv().AimPart = "Head" -- For R15 Games: {UpperTorso, LowerTorso, HumanoidRootPart, Head} | For R6 Games: {Head, Torso, HumanoidRootPart}
	getgenv().AimlockToggleKey = "Y" -- Toggles Aimbot On/Off 
	getgenv().AimRadius = 80 -- How far away from someones character you want to lock on at
	getgenv().ThirdPerson = false -- Locking onto someone in your Third Person POV
	getgenv().FirstPerson = true -- Locking onto someone in your First Person POV
	getgenv().TeamCheck = false -- Check if Target is on your Team (True means it wont lock onto your teamates, false is vice versa) (Set it to false if there are no teams)
	getgenv().PredictMovement = true -- Predicts if they are moving in fast velocity (like jumping) so the aimbot will go a bit faster to match their speed 
	getgenv().PredictionVelocity = 4 -- The speed of the PredictMovement feature 

	loadstring(game:HttpGet("https://pastebin.com/raw/g3fSf9xM", true))()
end)

SPEED.Name = "SPEED"
SPEED.Parent = Deszkv10
SPEED.BackgroundColor3 = Color3.fromRGB(79, 79, 79)
SPEED.BorderColor3 = Color3.fromRGB(0, 0, 0)
SPEED.Position = UDim2.new(0.683574855, 0, 1, 0)
SPEED.Size = UDim2.new(0, 131, 0, 34)
SPEED.Font = Enum.Font.SourceSans
SPEED.Text = "Speed [Q]"
SPEED.TextColor3 = Color3.fromRGB(0, 0, 0)
SPEED.TextSize = 14.000
SPEED.MouseButton1Down:connect(function()
plr = game:GetService('Players').LocalPlayer down = false  function onButton1Down(mouse)     down = true     while down do         if not down then break end         local char = plr.Character         char.HumanoidRootPart.Velocity = char.HumanoidRootPart.CFrame.lookVector * 170         wait()     end end  function onButton1Up(mouse)     down = false end  function onSelected(mouse)     mouse.KeyDown:connect(function(k) if k:lower()=="q"then onButton1Down(mouse)end end)     mouse.KeyUp:connect(function(k) if k:lower()=="q"then onButton1Up(mouse)end end) end onSelected(game.Players.LocalPlayer:GetMouse())
end)

TextBox.Parent = Deszkv10
TextBox.BackgroundColor3 = Color3.fromRGB(56, 56, 56)
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.Position = UDim2.new(0, 0, 1.68000031, 0)
TextBox.Size = UDim2.new(0, 414, 0, 161)
TextBox.Font = Enum.Font.SourceSans
TextBox.Text = "LA GUI ES FEA LOSE OK ESTA EN BETA SE ESTA TRABAJANDO EN OTRA GUI"
TextBox.TextColor3 = Color3.fromRGB(0, 0, 0)
TextBox.TextSize = 13.000

ANIMACIONES.Name = "ANIMACIONES"
ANIMACIONES.Parent = Deszkv10
ANIMACIONES.BackgroundColor3 = Color3.fromRGB(71, 71, 71)
ANIMACIONES.BorderColor3 = Color3.fromRGB(0, 0, 0)
ANIMACIONES.Position = UDim2.new(0.289855063, 0, 1.66000032, 0)
ANIMACIONES.Size = UDim2.new(0, 163, 0, 38)
ANIMACIONES.Font = Enum.Font.SourceSans
ANIMACIONES.Text = "Animaciones [Solo para alts]"
ANIMACIONES.TextColor3 = Color3.fromRGB(0, 0, 0)
ANIMACIONES.TextSize = 14.000
ANIMACIONES.MouseButton1Down:connect(function()
game.Players.LocalPlayer.Character.Animate.idle.Animation1.AnimationId = "http://www.roblox.com/asset/?id=616158929"
game.Players.LocalPlayer.Character.Animate.idle.Animation2.AnimationId = "http://www.roblox.com/asset/?id=616158929"
game.Players.LocalPlayer.Character.Animate.walk.WalkAnim.AnimationId = "http://www.roblox.com/asset/?id=616168032"
game.Players.LocalPlayer.Character.Animate.run.RunAnim.AnimationId = "http://www.roblox.com/asset/?id=616163682"
game.Players.LocalPlayer.Character.Animate.jump.JumpAnim.AnimationId = "http://www.roblox.com/asset/?id=1083218792"
game.Players.LocalPlayer.Character.Animate.fall.FallAnim.AnimationId = "http://www.roblox.com/asset/?id=1083189019"
game.Players.LocalPlayer.Character.Animate.jump.JumpAnim.AnimationId = "http://www.roblox.com/asset/?id=1083218792"
game.Players.LocalPlayer.Character.Animate.fall.FallAnim.AnimationId = "http://www.roblox.com/asset/?id=707829716"
end)
