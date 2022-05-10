--Library and Main
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Serkan Man Hub", "Synapse")
local Universal = Window:NewTab("Universal")
local HumanEdit = Universal:NewSection("Humanoid Editing")
HumanEdit:NewSlider("Set Walk Speed", "Sets your walk speed to value.", 216, 16, function(ws)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = ws
end)
HumanEdit:NewSlider("Set Jump Power", "Sets your jump power to value.", 350, 50, function(jp)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = jp
end)
HumanEdit:NewButton("Infinite Yield", "Nothing", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)
local Additions = Universal:NewSection("Additions")
Additions:NewButton("Rejoin", "Rejoins to the game", function()
    local Players = game.Players
    Players.LocalPlayer:Kick("\nRejoining...")
	wait()
	game:GetService('TeleportService'):Teleport(game.PlaceId, Players.LocalPlayer)
end)
Additions:NewKeybind("Toggle GUI", "Closes or Opens this GUI", Enum.KeyCode.RightShift, function()
	Library:ToggleUI()
end)
--Destruction Simulator
local DestSimTab = Window:NewTab("Destruction Simulator")
local DestSimSect = DestSimTab:NewSection("Hubs")
DestSimSect:NewButton("Aqua Modz Hub", "Nothing", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/AquaModz/DestructionSIMModded/main/DestructionSimAqua.lua'))()
end)
DestSimSect:NewButton("Fade Remix Hub", "Nothing", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/FadeRemix/RND-Games/main/DestructionSim.lua"))()
end)

--Star Simulator Beta
local StarSim = Window:NewTab("Star Simulator Beta")
local StarSimSect = StarSim:NewSection("Hubs")
StarSimSect:NewButton("Dark Hub", "Nothing", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/RandomAdamYT/DarkHub/master/Init", true))()
end)
local SerkanHubAdditions = StarSim:NewSection("Serkan Man Hub Additions")
SerkanHubAdditions:NewButton("Auto Farm (BROKEN)", "Starts auto farm", function()
    while _G.Autofarm == true do
        wait()
        local ok = tostring("Star_"..game.Players.LocalPlayer.Name)
        for i,v in pairs(game:GetService("Workspace")[ok].Player:GetDescendants()) do
        if v.ClassName == "Model" and v:FindFirstChild("RefreshHP") then
        game:GetService("ReplicatedStorage").Attack.UpdateHPEvent:FireServer(v, "Axe")
        game:GetService("ReplicatedStorage").Attack.UpdateHPEvent:FireServer(v, "Pickaxe")
        end
        end
        end
end)
SerkanHubAdditions:NewButton("See all world parts", "Nothing", function()
    local function unlockLand()
        for _, player in next, game.Players:GetChildren() do
            for _, land in next, workspace["Star_"..player.Name].Player.Land:GetChildren() do
                game.ReplicatedStorage.PlayerData.Unlocker.LandShow:FireServer(land)
            end
        end
    end

    game.Players.PlayerAdded:Connect(unlockLand)
    unlockLand()
end)
--Bedwars
local bedwars = Window:NewTab("Bedwars")
local bedwarsSect = bedwars:NewSection("Hubs")
bedwarsSect:NewButton("Vape Gui", "Nothing", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
end)
--Arsenal
local ArsenalT = Window:NewTab("Arsenal")
local ArsenalSect = ArsenalT:NewSection("Hubs")
ArsenalSect:NewButton("Nexus Hub", "Nothing", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/GwnStefano/NexusHub/main/Main", true))()
end)
--Super Power Tycoon
local spt = Window:NewTab("Super Power Tycoon")
local sptsect = spt:NewSection("Hubs")
sptsect:NewButton("IDK Hub", "Nothing", function()
    local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/AikaV3rm/UiLib/master/Lib.lua')))()
    local plrhead = game.Players.LocalPlayer.Character.Head


    local uimain = library:CreateWindow("Super Power Tycoon")


    local web = uimain:CreateFolder("Web Tycoon")


    web:Button("Get Web",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons["Web"].Door["ActDoor"], 0)
    end)

    web:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Web"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    web:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Web"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    web:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Web"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    web:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Web"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local giant = uimain:CreateFolder("Giant Tycoon")


    giant:Button("Get Giant",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Giant.Door["ActDoor"], 0)
    end)

    giant:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons.Giant.CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    giant:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons.Giant:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    giant:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons.Giant:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    giant:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons.Giant.Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local stone = uimain:CreateFolder("Stone Tycoon")


    stone:Button("Get Stone",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Stone.Door["ActDoor"], 0)
    end)

    stone:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Stone"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    stone:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Stone"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    stone:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Stone"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    stone:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Stone"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local robotic = uimain:CreateFolder("Robotic Tycoon")


    robotic:Button("Get Robotic",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Robotic.Door["ActDoor"], 0)
    end)

    robotic:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Robotic"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    robotic:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Robotic"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    robotic:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Robotic"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    robotic:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Robotic"].Spawn.CFrame * CFrame.new(0,5,0)
    end)


    local insanity = uimain:CreateFolder("Insanity Tycoon")

    insanity:Button("Get Insanity",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons["Insanity"].Door["ActDoor"], 0)
    end)

    insanity:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Insanity"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    insanity:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Insanity"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    insanity:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Insanity"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    insanity:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Insanity"].Spawn.CFrame * CFrame.new(0,5,0)
    end)


    local magic = uimain:CreateFolder("Magic Tycoon")

    magic:Button("Get Magic",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons["Magic"].Door["ActDoor"], 0)
    end)

    magic:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Magic"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    magic:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Magic"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    magic:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Magic"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    magic:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Magic"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local strong = uimain:CreateFolder("Strong Tycoon")

    strong:Button("Get Strong",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons["Strong"].Door["ActDoor"], 0)
    end)

    strong:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Strong"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    strong:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Strong"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    strong:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Strong"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    strong:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Strong"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local storm = uimain:CreateFolder("Storm Tycoon")


    storm:Button("Get Storm",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Storm.Door["ActDoor"], 0)
    end)


    storm:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Storm"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    storm:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Storm"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    storm:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Storm"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    storm:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Storm"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local dark = uimain:CreateFolder("Dark Tycoon")


    dark:Button("Get Dark",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Dark.Door["ActDoor"], 0)
    end)

    dark:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Dark"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    dark:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Dark"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    dark:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Dark"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    dark:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Dark"].Spawn.CFrame * CFrame.new(0,5,0)
    end)



    local spike = uimain:CreateFolder("Spike Tycoon")


    spike:Button("Get Tailed",function()
        firetouchinterest(plrhead, game.Workspace.Tycoons.Spike.Door["ActDoor"], 0)
    end)

    spike:Toggle("Cash AutoGrab",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.2) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Spike"].CashRegister.Ching:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end
                end
            end
        end
    end)

    spike:Button("Get All My Tools",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons["Spike"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    spike:Toggle("AutoBuy",function(bool)
        shared.toggle = bool
        if shared.toggle == true then
            while wait(.5) do
                if shared.toggle == false then break end
            for i,v in pairs(game:GetService("Workspace").Tycoons["Spike"]:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent then
                    if v.Parent.Parent.Name ~= "Robux1" then
                    if v.Parent.Parent.Name ~= "Robux2" then
                    if v.Parent.Name ~= "Ching" then
                    if v.Parent.Parent.Name ~= "LegendaryGear" then
                    if v.Parent.Parent.Name ~= "VoidShield" then 
                    if v.Parent.Parent.Name ~= "ShopModel" then
                        firetouchinterest(plrhead, v.Parent, 0)
                        wait(0.01)
                        firetouchinterest(plrhead, v.Parent, 1)
                    end end end end end end
                    end
                end
            end
        end
    end)

    spike:Button("TP to Spawn",function()
        plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Spike"].Spawn.CFrame * CFrame.new(0,5,0)
    end)

    local others = uimain:CreateFolder("Others")
    others:Button("Get All Tools [LOADED!]",function()
            for i,v in pairs(game:GetService("Workspace").Tycoons:GetDescendants()) do
                if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
                firetouchinterest(plrhead, v.Parent, 0)
                wait(0.01)
                firetouchinterest(plrhead, v.Parent, 1)
            end
        end
    end)

    others:Label("Credit to Muzan QLTN",{
        TextSize = 20; -- Self Explaining
        TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
        BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
        
    })
    others:Label("(on youtube)",{
        TextSize = 20; -- Self Explaining
        TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
        BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
        
    })
end)
--Ultra Power Tycoon
local upt = Window:NewTab("Ultra Power Tycoon")
local uptsect = upt:NewSection("Hubs")
uptsect:NewButton("IDK Hub", "Nothing", function()
    local library = loadstring(game:HttpGet(('https://raw.githubusercontent.com/AikaV3rm/UiLib/master/Lib.lua')))()
local plrhead = game.Players.LocalPlayer.Character.Head


local uimain = library:CreateWindow("Ultra Power Tycoon")


local woodmaster = uimain:CreateFolder("Wood Master Tycoon")


woodmaster:Button("Get Wood Master",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons["Get Wood Master"].Door["ActDoor"], 0)
end)

woodmaster:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Wood Master"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

woodmaster:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Wood Master"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

woodmaster:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Wood Master"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

woodmaster:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Wood Master"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local push = uimain:CreateFolder("Push Tycoon")


push:Button("Get Push",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Push.Door["ActDoor"], 0)
end)

push:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons.Push.CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

push:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons.Push:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

push:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons.Push:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

push:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons.Push.Spawn.CFrame * CFrame.new(0,5,0)
end)



local rage = uimain:CreateFolder("Rage Tycoon")


rage:Button("Get Rage",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Rage.Door["ActDoor"], 0)
end)

rage:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Rage"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

rage:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Rage"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

rage:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Rage"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

rage:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Rage"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local eternal = uimain:CreateFolder("Eternal Tycoon")


eternal:Button("Get Eternal",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Eternal.Door["ActDoor"], 0)
end)

eternal:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Eternal"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

eternal:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Eternal"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

eternal:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Eternal"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

eternal:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Eternal"].Spawn.CFrame * CFrame.new(0,5,0)
end)


local sandlord = uimain:CreateFolder("Sand Lord Tycoon")

sandlord:Button("Get Sand Lord",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons["Sand Lord"].Door["ActDoor"], 0)
end)

sandlord:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sand Lord"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

sandlord:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sand Lord"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

sandlord:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sand Lord"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

sandlord:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Sand Lord"].Spawn.CFrame * CFrame.new(0,5,0)
end)


local deatheye = uimain:CreateFolder("Death Eye Tycoon")

deatheye:Button("Get Death Eye",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons["Death Eye"].Door["ActDoor"], 0)
end)

deatheye:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Death Eye"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

deatheye:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Death Eye"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

deatheye:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Death Eye"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

deatheye:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Death Eye"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local darkflame = uimain:CreateFolder("Dark Flame Tycoon")

darkflame:Button("Get Dark Flame",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons["Dark Flame"].Door["ActDoor"], 0)
end)

darkflame:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Dark Flame"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

darkflame:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Dark Flame"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

darkflame:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Dark Flame"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

darkflame:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Dark Flame"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local sneak = uimain:CreateFolder("Sneak Tycoon")


sneak:Button("Get Sneak",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Sneak.Door["ActDoor"], 0)
end)


sneak:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sneak"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

sneak:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sneak"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

sneak:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Sneak"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

sneak:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Sneak"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local cursed = uimain:CreateFolder("Cursed Tycoon")


cursed:Button("Get Cursed",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Cursed.Door["ActDoor"], 0)
end)

cursed:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Cursed"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

cursed:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Cursed"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

cursed:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Cursed"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

cursed:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Cursed"].Spawn.CFrame * CFrame.new(0,5,0)
end)



local tailed = uimain:CreateFolder("Tailed Tycoon")


tailed:Button("Get Tailed",function()
    firetouchinterest(plrhead, game.Workspace.Tycoons.Tailed.Door["ActDoor"], 0)
end)

tailed:Toggle("Cash AutoGrab",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.2) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Tailed"].CashRegister.Ching:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end
            end
        end
    end
end)

tailed:Button("Get All My Tools",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons["Tailed"]:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

tailed:Toggle("AutoBuy",function(bool)
    shared.toggle = bool
    if shared.toggle == true then
        while wait(.5) do
            if shared.toggle == false then break end
        for i,v in pairs(game:GetService("Workspace").Tycoons["Tailed"]:GetDescendants()) do
             if v.Name == "TouchInterest" and v.Parent then
                if v.Parent.Parent.Name ~= "Robux1" then
                if v.Parent.Parent.Name ~= "Robux2" then
                if v.Parent.Name ~= "Ching" then
                if v.Parent.Parent.Name ~= "LegendaryGear" then
                if v.Parent.Parent.Name ~= "VoidShield" then 
                if v.Parent.Parent.Name ~= "ShopModel" then
                    firetouchinterest(plrhead, v.Parent, 0)
                    wait(0.01)
                    firetouchinterest(plrhead, v.Parent, 1)
                end end end end end end
                end
            end
        end
    end
end)

tailed:Button("TP to Spawn",function()
    plrhead.Parent.HumanoidRootPart.CFrame = game:GetService("Workspace").Tycoons["Tailed"].Spawn.CFrame * CFrame.new(0,5,0)
end)

local others = uimain:CreateFolder("Others")
others:Button("Get All Tools [LOADED!]",function()
        for i,v in pairs(game:GetService("Workspace").Tycoons:GetDescendants()) do
            if v.Name == "TouchInterest" and v.Parent.Name == "Neon"  then
            firetouchinterest(plrhead, v.Parent, 0)
            wait(0.01)
            firetouchinterest(plrhead, v.Parent, 1)
         end
     end
end)

others:Label("Credit to SerkanMan",{
    TextSize = 20; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
})
others:Label("(me) youtube",{
    TextSize = 20; -- Self Explaining
    TextColor = Color3.fromRGB(255,255,255); -- Self Explaining
    BgColor = Color3.fromRGB(69,69,69); -- Self Explaining
    
})
end)




