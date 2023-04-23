    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("PG HUB", "Synapse")
local Tab = Window:NewTab("All in one")
local Section = Tab:NewSection("AUTO Fram")
Section:NewToggle("Auto Farm", "Lv1 - ???", function(state)
    
_G.Auto_Farm = state

function totarget(p)
    local Distance2 = (p.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new(Distance2/350, Enum.EasingStyle.Linear)
    local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = p})
    tween:Play()
    if Distance2 <= 75 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
    end
end

function checklevel()
    local lv = game:GetService("Players").LocalPlayer.Data.Level.Value
    if lv == 1 or lv <= 9 then
        Mon = "Bandit [Lv. 5]"
        Title = "Bandit"
        QuestName = "BanditQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(1061.15271, 16.7367725, 1548.93018, -0.836085379, -3.89774577e-08, 0.548599303, -1.17575967e-08, 1, 5.31300408e-08, -0.548599303, 3.79710414e-08, -0.836085379)
        CFrameMon = CFrame.new(1151.11829, 16.7761021, 1599.73499, -0.999999762, 0, -0.000701809535, 0, 1, 0, 0.000701809535, 0, -0.999999762)
        CFramePuk = CFrame.new(1101.75903, 67.6758957, 1617.50391, -0.399259984, -5.24373327e-08, -0.916837752, -1.74068084e-08, 1, -4.96134582e-08, 0.916837752, -3.84945009e-09, -0.399259984)
    elseif lv == 10 or lv <= 14 then
        Mon = "Monkey [Lv. 14]"
        Title = "Monkey"
        QuestName = "JungleQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1479.76099, 23.195364, 106.327942, 0.96289885, 5.22265786e-10, -0.269862473, 6.59528099e-10, 1, 4.28857172e-09, 0.269862473, -4.30744285e-09, 0.96289885)
        CFramePuk = CFrame.new(-1776.32959, 61.1782455, 66.8902054, -0.912609756, -2.38546143e-08, 0.408831745, -2.14773621e-08, 1, 1.04056577e-08, -0.408831745, 7.15677129e-10, -0.912609756)
        elseif lv == 15 or lv <= 29 then
        Mon = "Gorilla [Lv. 20]"
        Title = "Gorilla"
        QuestName = "JungleQuest"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1599.23096, 37.8653831, 153.335953, -0.0493941903, 1.29583286e-08, 0.998779356, 3.21716165e-08, 1, -1.13831318e-08, -0.998779356, 3.15700852e-08, -0.0493941903)
        CFrameMon = CFrame.new(-1242.46655, 6.62262297, -523.166382, -0.974416733, 9.23166681e-08, -0.224748924, 9.58993027e-08, 1, -5.02435071e-09, 0.224748924, -2.64490758e-08, -0.974416733)
        CFramePuk = CFrame.new(-1133.4574, 40.8067436, -526.086792, 0.647179008, -2.76535794e-10, 0.762338042, 3.26674865e-08, 1, -2.73699801e-08, -0.762338042, 4.26169464e-08, 0.647179008)
        elseif lv == 30 or lv <= 39 then
        Mon = "Pirate [Lv. 35]"
        Title = "Pirate"
        QuestName = "BuggyQuest1"
        QuestNumber = 1
        CFrameQuest = CFrame.new(-1140.73157, 5.15205145, 3830.37183, -0.95384413, 1.34328193e-08, 0.300302118, -1.75551698e-08, 1, -1.00491178e-07, -0.300302118, -1.01124776e-07, -0.95384413)
        CFrameMon = CFrame.new(-1207.77466, 4.7520504, 3913.94971, -0.482618034, 7.00762115e-08, 0.875830948, 7.80261011e-09, 1, -7.57115686e-08, -0.875830948, -2.97059994e-08, -0.482618034)
        CFramePuk = CFrame.new(-1159.01782, 44.7520294, 3846.146, 0.961922944, -3.43352333e-08, -0.273320764, 3.62712917e-08, 1, 2.0304145e-09, 0.273320764, -1.18667991e-08, 0.961922944)
        elseif lv == 40 or lv <= 59 then
        Mon = "Brute [Lv. 45]"
        Title = "Brute"
        QuestName = "BuggyQuest1"
        QuestNumber = 2
        CFrameQuest = CFrame.new(-1140.73157, 5.15205145, 3830.37183, -0.95384413, 1.34328193e-08, 0.300302118, -1.75551698e-08, 1, -1.00491178e-07, -0.300302118, -1.01124776e-07, -0.95384413)
        CFrameMon = CFrame.new(-1331.67627, 14.8698673, 4282.48633, 0.0249894615, 3.82893856e-10, -0.999687731, -1.1674242e-08, 1, 9.11893061e-11, 0.999687731, 1.16683179e-08, 0.0249894615)
        CFramePuk = CFrame.new(-1435.45996, 26.4277897, 4279.23779, -0.0853926614, 2.70740458e-10, -0.996347368, 5.79785358e-08, 1, -4.6973585e-09, 0.996347368, -5.81678812e-08, -0.0853926614)
                elseif lv == 60 or lv <= 84 then
        Mon = "Desert Bandit [Lv. 60]"
        Title = "Desert Bandit"
        QuestName = "DesertQuest"
        QuestNumber = 1
        CFrameQuest = CFrame.new(894.582825, 6.43846273, 4394.17285, 0.904637039, 5.12283833e-08, -0.426182866, -2.90814555e-08, 1, 5.84730699e-08, 0.426182866, -4.05028864e-08, 0.904637039)
        CFrameMon = CFrame.new(920.140991, 6.44889307, 4477.95215, -0.730570138, 4.74096851e-09, -0.682837665, 1.93753902e-09, 1, 4.87005991e-09, 0.682837665, 2.23489582e-09, -0.730570138)
        CFramePuk = CFrame.new(863.341187, 15.1284752, 4414.90137, -0.909780681, -4.28535678e-08, -0.415089309, -3.35608945e-08, 1, -2.96816047e-08, 0.415089309, -1.30729818e-08, -0.909780681)
    end
end

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
totarget(CFrameQuest)
wait(.3)
local args = {
    [1] = "StartQuest",
    [2] = QuestName,
    [3] = QuestNumber
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        for i,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon and v2.Name == Mon then
            totarget(v.HumanoidRootPart.CFrame * CFrame.new(0,1,15))
            v.HumanoidRootPart.Size = Vector3.new(60,2.5,60)
            v.HumanoidRootPart.CFrame = CFrameMon
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
            v2.HumanoidRootPart.CanCollide = false
            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
        end
        end
    end
                end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, Title) then
local args = {
    [1] = "AbandonQuest"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            if not game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
                totarget(CFramePuk)
            end
            end
        end)
    end
end)

spawn(function()
    while task.wait(.1) do
        pcall(function()
            if _G.Auto_Farm then
            checklevel()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
        if v.Name == Mon then
            if v.Humanoid.Health == 0 then
            v:Destroy()
            end
            end
            end
            end
        end)
    end
end)
end)


local Section = Tab:NewSection("Auto Equip")

local Weaponlist = {}
local Weapon = nil

for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    table.insert(Weaponlist,v.Name)
end

Section:NewDropdown("select weapon", " ", Weaponlist, function(currentOption)
    Weapon = currentOption
end)

Section:NewToggle("Auto Equip", " ", function(a)
AutoEquiped = a
end)

spawn(function()
while wait() do
if AutoEquiped then
pcall(function()
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
end)
end
end
end)
local Tab = Window:NewTab("AUTO Stat")
local Section = Tab:NewSection("AUTO Stat")
Section:NewToggle("Melee", "ToggleInfo", function(state)
    _G.melee = state 
    while _G.melee do wait()
    local args = {
    [1] = "AddPoint",
    [2] = "Melee",
    [3] = 1
}

game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
end
end)

local Tab = Window:NewTab("Buy")
local Section = Tab:NewSection("ALL")
Section:NewButton("BuyBlackLeg V1", "BuyBlackLeg", function()
        local args = {
    [1] = "BuyBlackLeg"
}

game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
end)





