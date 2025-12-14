local main = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local up = Instance.new("TextButton")
local down = Instance.new("TextButton")
local onoff = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local plus = Instance.new("TextButton")
local speed = Instance.new("TextLabel")
local mine = Instance.new("TextButton")
local closebutton = Instance.new("TextButton")
local mini = Instance.new("TextButton")
local mini2 = Instance.new("TextButton")

main.Name = "wbin"
main.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
main.IgnoreGuiInset = true
main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
main.ResetOnSpawn = false

Frame.Parent = main
Frame.BackgroundColor3 = Color3.fromRGB(163, 255, 137)
Frame.BorderColor3 = Color3.fromRGB(133, 221, 213)
Frame.Position = UDim2.new(0.100320618, 0, 0.379746825, 0)
Frame.Size = UDim2.new(0, 190, 0, 57)
Frame.SliderVisible = true
Frame.Visible = true

up.Name = "up"
up.Parent = Frame
up.BackgroundColor3 = Color3.fromRGB(79, 255, 152)
up.Position = UDim2.new(0, 34, 0, 28)
up.Size = UDim2.new(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
up.Text = "UP"
up.TextColor3 = Color3.fromRGB(0, 0, 0)
up.TextSize = 14.000

down.Name = "down"
down.Parent = Frame
down.BackgroundColor3 = Color3.fromRGB(215, 255, 121)
down.Position = UDim2.new(0, 34, 0, 491228074, 0)
down.Size = UDim2.new(0, 44, 0, 28)
down.Font = Enum.Font.SourceSans
down.Text = "DOWN"
down.TextColor3 = Color3.fromRGB(0, 0, 0)
down.TextSize = 14.000

onoff.Name = "onoff"
onoff.Parent = Frame
onoff.BackgroundColor3 = Color3.fromRGB(255, 249, 74)
onoff.Position = UDim2.new(0.708232681, 0, 0.491228074, 0)
onoff.Size = UDim2.new(0, 44, 0, 28)
onoff.Font = Enum.Font.SourceSans
onoff.Text = "fly"
onoff.TextColor3 = Color3.fromRGB(0, 0, 0)
onoff.TextSize = 14.000

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(242, 60, 255)
TextLabel.Position = UDim2.new(0.000, 0, 0.46932701, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 70, 0, 28)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "FLY GUI V3"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

plus.Name = "plus"
plus.Parent = Frame
plus.BackgroundColor3 = Color3.fromRGB(131, 145, 255)
plus.Position = UDim2.new(0.231578946, 0, 0, 0, 0, 0)
plus.Size = UDim2.new(0, 44, 0, 28)
plus.Font = Enum.Font.SourceSans
plus.Text = "+"
plus.TextColor3 = Color3.fromRGB(0, 0, 0)
plus.TextScaled = true
plus.TextSize = 14.000
plus.TextWrapped = true

speed.Name = "speed"
speed.Parent = Frame
speed.BackgroundColor3 = Color3.fromRGB(255, 85, 0)
speed.Position = UDim2.new(0.48421021, 0, 0.491228074, 0)
speed.Size = UDim2.new(0, 44, 0, 28)
speed.Font = Enum.Font.SourceSans
speed.Text = ""
speed.TextColor3 = Color3.fromRGB(0, 0, 0)
speed.TextScaled = true
speed.TextSize = 14.000
speed.TextWrapped = true

mine.Name = "mine"
mine.Parent = Frame
mine.BackgroundColor3 = Color3.fromRGB(123, 255, 247)
mine.Position = UDim2.new(0.45, 0, 0.231578946, 0, 0.491228074, 0)
mine.Size = UDim2.new(0, 45, 0, 29)
mine.Font = Enum.Font.SourceSans
mine.Text = "-"
mine.TextColor3 = Color3.fromRGB(0, 0, 0)
mine.TextScaled = true
mine.TextSize = 14.000
mine.TextWrapped = true

closebutton.Name = "close"
closebutton.Parent = main
closebutton.BackgroundColor3 = Color3.fromRGB(255, 25, 0)
closebutton.Position = UDim2.new(0, 45, 0, 28)
closebutton.Size = UDim2.new(0, 45, 0, 28)
closebutton.Font = Enum.Font.SourceSans
closebutton.Text = "X"
closebutton.TextSize = 30.000
closebutton.Position = UDim2.new(0, 0, -1, 27)

mini.Name = "minimize"
mini.Parent = main
mini.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
mini.Position = UDim2.new(0, 45, 0, 28)
mini.Size = UDim2.new(0, 45, 0, 28)
mini.Font = Enum.Font.SourceSans
mini.Text = "-"
mini.TextSize = 40.000
mini.Position = UDim2.new(0, 44, -1, 27)

mini2.Name = "minimize2"
mini2.Parent = main
mini2.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
mini2.Position = UDim2.new(0, 45, 0, 28)
mini2.Size = UDim2.new(0, 45, 0, 28)
mini2.Font = Enum.Font.SourceSans
mini2.Text = "+"
mini2.TextSize = 40.000
mini2.Position = UDim2.new(0, 44, -1, 57)
mini2.Visible = false

speeds = 1

local speaker = game:GetService("Players").LocalPlayer
local chr = game.Players.LocalPlayer.Character
local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
nowe = false
nome = false

game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "FLY GUI V3";
    Text = "BY XMEO";
    Icon = "rbxassetid://5107182114&isAvatar=true&150&h=150";
    Duration = 5;
    Button1 = "Close";
})

main.Visible = true
Frame.Active = true -- main gui
Frame.Draggable = true

onoff.MouseButton1Down:connect(function()
    if nowe == true then
        nowe = false
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics, true)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming, true)
    else
        nowe = true
        for i = 1, speeds do
            spawn(function()
                local hb = game:GetService("RunService").Heartbeat
                tpwalking = true
                local chr = game.Players.LocalPlayer.Character
                local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
                while tpwalking and chr and wait() and chr and hum and hum.Parent do
                    if hum.MoveDirection.Magnitude ~= 0 then
                        chr:TranslateBy(hum.MoveDirection)
                    end
                end
            end)
        end
        game.Players.LocalPlayer.Character.Animate.Disabled = true
        local Char = game.Players.LocalPlayer.Character
        local Hum = Char:FindFirstChildOfClass("Humanoid") or Char:FindFirstChildOfClass("AnimationController")
        if not Hum then return end
        for i, v in next, Hum:GetPlayingAnimationTracks() do
            v:AdjustSpeed(0)
        end
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics, false)
        speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming, false)
        speaker.Character.Humanoid:ChangeState(Enum.HumanoidStateType.Swimming)
    end

    if game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then
        local plr = game.Players.LocalPlayer
        local torso = plr.Character.Torso
        local flying = true
        local deb = false
        local ctrl = {f = 0, b = 0, l = 0, r = 0}
        local lastctrl = {f = 0, b = 0, l = 0, r = 0}
        local maxspeed = 50
        local speed = 0
        local s = 0

        local bg = Instance.new("BodyGyro", torso)
        bg.P = 9e4
        bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
        bg.cframe = torso.CFrame
        local bv = Instance.new("BodyVelocity", torso)
        bv.velocity = Vector3.new(0, 0, 0)
        bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
        if nowe == true then
            plr.Character.Humanoid.PlatformStand = true
        end
        while nowe == true or game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 do
            game:GetService("RunService").RenderStepped:wait()
            if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then
                speed = speed + 0.5*(speed/maxspeed)
                if speed > maxspeed then
                    speed = maxspeed
                end
            elseif not (ctrl.l + ctrl.r == 0 or ctrl.f + ctrl.b == 0) and speed ~= 0 then
                speed = speed - 0.1
                if speed < 0 then
                    speed = 0
                end
            end

            if (ctrl.l + ctrl.r) == 0 or (ctrl.f + ctrl.b) == 0 then
                bv.velocity = (game.Workspace.CurrentCamera.CFrame.LookVector * (ctrl.f - ctrl.b) + 
                               (game.Workspace.CurrentCamera.CFrame * CFrame.new(ctrl.r - ctrl.l, 0, 0)).LookVector * (ctrl.r + ctrl.l)) * speed
                game.Workspace.CurrentCamera.CFrame = (f * speed, b = ctrl.b, l = ctrl.l, r = ctrl.r)
                lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
            elseif (ctrl.l + ctrl.r) ~= 0 and (ctrl.f + ctrl.b) ~= 0 and speed ~= 0 then
                bv.velocity = (game.Workspace.CurrentCamera.CFrame.LookVector * (lastctrl.f - lastctrl.b) + 
                               (game.Workspace.CurrentCamera.CFrame * CFrame.new(lastctrl.r - lastctrl.l, 0, 0)).LookVector * (lastctrl.r + lastctrl.l)) * speed
                game.Workspace.CurrentCamera.CFrame = game.Workspace.CurrentCamera.CFrame * CFrame.new(0, 0, 0)
            else
                bv.velocity = Vector3.new(0, 0, 0)
            end

            game.Players.LocalPlayer.Character.Animate.Disabled = true
            bg.cframe = game.Workspace.CurrentCamera.CFrame * CFrame.Angles(-math.rad(ctrl.f * speed / maxspeed * 0.0), 0, 0)
            ctrl = {f = 0, b = 0, l = 0, r = 0}
            lastctrl = {f = 0, b = 0, l = 0, r = 0}
            speed = 0
            bg:Destroy()
            bv:Destroy()
            plr.Character.Humanoid.PlatformStand = false
            game.Players.LocalPlayer.Character.Animate.Disabled = false
            tpwalking = false
        end
    else
        local plr = game.Players.LocalPlayer
        local UpperTorso = plr.Character.UpperTorso
        local deb = true
        local flying = true
        local ctrl = {f = 0, b = 0, l = 0, r = 0}
        local lastctrl = {f = 0, b = 0, l = 0, r = 0}
        local maxspeed = 50
        local speed = 0
        local s = 0

        local bg = Instance.new("BodyGyro", UpperTorso)
        bg.P = 9e4
        bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
        bg.cframe = UpperTorso.CFrame
        local bv = Instance.new("BodyVelocity", UpperTorso)
        bv.velocity = Vector3.new(0, 0, 0)
        bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
        if nowe == true then
            plr.Character.Humanoid.PlatformStand = true
        end
        while nowe == true or game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 do
            wait()
            if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then
                speed = speed + 0.5*(speed/maxspeed)
                if speed > maxspeed then
                    speed = maxspeed
                end
            elseif (ctrl.l + ctrl.r == 0 or ctrl.f + ctrl.b == 0) and speed ~= 0 then
                speed = speed - 0.1
                if speed < 0 then
                    speed = 0
                end
            end

            if (ctrl.l + ctrl.r) == 0 or (ctrl.f + ctrl.b) == 0 then
                bv.velocity = (game.Workspace.CurrentCamera.CFrame.LookVector * (ctrl.f - ctrl.b) + 
                               (game.Workspace.CurrentCamera.CFrame * CFrame.new(ctrl.r - ctrl.l, 0, 0)).LookVector * (ctrl.r + ctrl.l)) * speed
                game.Workspace.CurrentCamera.CFrame = game.Workspace.CurrentCamera.CFrame * CFrame.new(0, 0, 0)
                lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
            elseif (ctrl.l + ctrl.r) ~= 0 and (ctrl.f + ctrl.b) ~= 0 and speed ~= 0 then
                bv.velocity = (game.Workspace.CurrentCamera.CFrame.LookVector * (lastctrl.f - lastctrl.b) + 
                               (game.Workspace.CurrentCamera.CFrame * CFrame.new(lastctrl.r - lastctrl.l, 0, 0)).LookVector * (lastctrl.r + lastctrl.l)) * speed
                game.Workspace.CurrentCamera.CFrame = game.Workspace.CurrentCamera.CFrame * CFrame.new(0, 0, 0)
            else
                bv.velocity = Vector3.new(0, 0, 0)
            end

            game.Players.LocalPlayer.Character.Animate.Disabled = true
            bg.cframe = game.Workspace.CurrentCamera.CFrame * CFrame.Angles(-math.rad(ctrl.f * speed / maxspeed * 0.0), 0, 0)
            ctrl = {f = 0, b = 0, l = 0, r = 0}
            lastctrl = {f = 0, b = 0, l = 0, r = 0}
            speed = 0
            bg:Destroy()
            bv:Destroy()
            plr.Character.Humanoid.PlatformStand = false
            game.Players.LocalPlayer.Character.Animate.Disabled = false
            tpwalking = false
        end
    end
end)

local tis
up.MouseButton1Down:connect(function()
    tis = up.MouseDown:connect(function()
        while true do
            wait()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = 
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0, 1, 0)
        end
    end)
end)
up.MouseLeave:connect(function()
    if tis then
        tis:disconnect()
    end
    tis = nil
end)

local dis
down.MouseButton1Down:connect(function()
    dis = down.MouseDown:connect(function()
        while true do
            wait()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = 
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0, -1, 0)
        end
    end)
end)
down.MouseLeave:connect(function()
    if dis then
        dis:disconnect()
    end
    dis = nil
end)

game:GetService("Players").LocalPlayer.CharacterAdded:connect(function(char)
    game.Players.LocalPlayer.Character.Humanoid.PlatformStand = false
    wait(0.7)
    game.Players.LocalPlayer.Character.Animate.Disabled = false
end)

plus.MouseButton1Down:connect(function()
    speed.Text = speeds
    if nowe == true then
        speeds = speeds + 1
        for i = 1, speeds do
            spawn(function()
                local hb = game:GetService("RunService").Heartbeat
                tpwalking = true
                local chr = game.Players.LocalPlayer.Character
                local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
                while tpwalking and chr and wait() and chr and hum and hum.Parent do
                    if hum.MoveDirection.Magnitude ~= 0 then
                        chr:TranslateBy(hum.MoveDirection)
                    end
                end
            end)
        end
    end
end)

mine.MouseButton1Down:connect(function()
    if speeds > 1 then
        speeds = speeds - 1
        speed.Text = speeds
    else
        speeds = speeds - 1
        speed.Text = speeds
        tpwalking = false
        for i = 1, speeds do
            spawn(function()
                local hb = game:GetService("RunService").Heartbeat
                tpwalking = true
                local chr = game.Players.LocalPlayer.Character
                local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
                while tpwalking and chr and wait() and chr and hum and hum.Parent do
                    if hum.MoveDirection.Magnitude ~= 0 then
                        chr:TranslateBy(hum.MoveDirection)
                    end
                end
            end)
        end
    end
end)

closebutton.MouseButton1Click:connect(function()
main:销毁()
结束)

结束)
向上。可见=假
下去。可见=假
另外。可见=假
我的。可见=假
主要的背景透明度= 1
迷你。可见=假
迷你2。可见=真
迷你2。Position = UDim2.new(0，44，-1，57)
结束)

迷你2。鼠标按钮1Click:connect(函数()
向上。可见=真
下去。可见=真
另外。可见=真
我的。可见=真
主要的背景透明度= 0
迷你。可见=真
迷你2。可见=假
迷你2。Position = UDim2.new(0，44，-1，27)
结束)
