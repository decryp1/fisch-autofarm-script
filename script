local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "sigma fisch script by decryp1",
   LoadingTitle = "very sigma script",
   LoadingSubtitle = "by decryp1",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil,
      FileName = "decryp1's fisch script"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink",
      RememberJoins = true
   },
   KeySystem = false,
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided",
      FileName = "Key",
      SaveKey = true,
      GrabKeyFromSite = false,
      Key = {"Hello"}
   }
})

local FishingTab = Window:CreateTab("Main")

local loopEnabled = false
local function resizeButtonLoop()
    while loopEnabled do
        local buttonPath = game:GetService("Players").LocalPlayer:FindFirstChild("PlayerGui")
            and game.Players.LocalPlayer.PlayerGui:FindFirstChild("shakeui")
            and game.Players.LocalPlayer.PlayerGui.shakeui:FindFirstChild("safezone")
            and game.Players.LocalPlayer.PlayerGui.shakeui.safezone:FindFirstChild("button")

        if buttonPath then
            buttonPath.Size = UDim2.new(0, 2000, 0, 2000)
            buttonPath.BackgroundTransparency = 1
        else
            print("did not find a button in the path!?!?")
        end
        wait(0.01)
    end
end

FishingTab:CreateToggle({
   Name = "change shake size",
   CurrentValue = false,
   Flag = "ToggleResize",
   Callback = function(Value)
       loopEnabled = Value
       if loopEnabled then
           resizeButtonLoop()
       end
   end,
})

FishingTab:CreateButton({
    Name = "perfect cast",
    Callback = function()
        local args = {
            [1] = 100,
            [2] = 2
        }
        local rod = game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flimsy Rod")
        if rod then
            rod.events.cast:FireServer(unpack(args))
        else
            warn("Flimsy Rod not found in character.")
        end
    end
})

FishingTab:CreateButton({
    Name = "perfect reel",
    Callback = function()
        local args = {
            [1] = 100,
            [2] = true
        }
        local reelfinished = game:GetService("ReplicatedStorage"):WaitForChild("events"):WaitForChild("reelfinished")
        reelfinished:FireServer(unpack(args))
    end
})

local clickingEnabled = false

local function startClicking()
    while clickingEnabled do
        local button = game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("TargetButton")
        if button and button:IsA("TextButton") then
            button.MouseButton1Click:Fire()
        end
        wait(0.1)
    end
end

FishingTab:CreateToggle({
    Name = "Auto GUI Click",
    CurrentValue = false,
    Flag = "AutoClickToggle",
    Callback = function(Value)
        clickingEnabled = Value
        if clickingEnabled then
            startClicking()
        end
    end,
})

local farmEnabled = false

local function startAutoFarm()
    while farmEnabled do
        local rod = game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flimsy Rod")
        if rod then
            local castArgs = { [1] = 100, [2] = 2 }
            rod.events.cast:FireServer(unpack(castArgs))
        else
            warn("Flimsy Rod not equipped.")
            break
        end

        local shakeGui = game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("shakeui")
        if shakeGui then
            repeat wait(0.1) until not shakeGui or not shakeGui:FindFirstChild("safezone") or not shakeGui.safezone:FindFirstChild("button") or not shakeGui.safezone.button.Visible
        end

        local reelGui = game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("reel")
        if reelGui then
            wait(1)
            while reelGui and farmEnabled do
                local reelArgs = { [1] = 100, [2] = true }
                local reelfinished = game:GetService("ReplicatedStorage"):WaitForChild("events"):WaitForChild("reelfinished")
                reelfinished:FireServer(unpack(reelArgs))
                wait(0.1)
                reelGui = game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("reel")
            end
        end
        wait(1)
    end
end

FishingTab:CreateToggle({
    Name = "Enable Auto-Farm",
    CurrentValue = false,
    Flag = "AutoFarmToggle",
    Callback = function(Value)
        farmEnabled = Value
        if farmEnabled then
            startAutoFarm()
        end
    end,
})

local TeleportTab = Window:CreateTab("Teleports")

-- Roslit Bay
TeleportTab:CreateButton({
    Name = "Roslit Bay",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1456.52075, 149.100327, 634.93042, -0.220467597, 0.277655303, -0.935040891, -6.47796794e-09, 0.958628654, 0.284659594, 0.975394249, 0.0627582148, -0.211346567)
    end
})

-- Moosewood
TeleportTab:CreateButton({
    Name = "Moosewood",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(368.19754, 140.309189, 239.525116, 0.00545042939, -0.557368159, 0.830247462, 1.31329436e-08, 0.8302598, 0.557376444, -0.999985099, -0.00303793023, 0.00452528009)
    end
})

-- Sunstone Island
TeleportTab:CreateButton({
    Name = "Sunstone Island",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-953.446106, 237.097076, -984.763611, 0.0270711854, 0.476107657, -0.878969967, -3.18643879e-06, 0.879292369, 0.476282239, 0.999633372, -0.0128907235, 0.0238050036)
    end
})

-- Mushgrove Swamp
TeleportTab:CreateButton({
    Name = "Mushgrove Swamp",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2687.99609, 140.724457, -731.668396, -0.891952872, -0.183939889, 0.413020432, -3.47988544e-06, 0.913505971, 0.406825155, -0.452128053, 0.362867445, -0.814804971)
    end
})

-- Terrapin Island
TeleportTab:CreateButton({
    Name = "Terrapin Island",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-172.422119, 149.404449, 1954.48059, 0.228378206, -0.496471673, 0.837471724, -3.02317221e-06, 0.860204518, 0.509949088, -0.973572373, -0.116463766, 0.196450472)
    end
})

-- Vertigo
TeleportTab:CreateButton({
    Name = "Vertigo",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-112.007278, -492.901093, 1040.32788, -1, 0, 0, 0, 1, 0, 0, 0, -1)
    end
})

-- Snowcap Island
TeleportTab:CreateButton({
    Name = "Snowcap Island",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2607.62256, 143.206451, 2396.54297, -0.953667223, -0.236189753, 0.18636784, -1.3614017e-06, 0.61944747, 0.785037994, -0.300863057, 0.748664856, -0.590747058)
    end
})

-- Keepars Altar
TeleportTab:CreateButton({
    Name = "Keepars Altar",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1296.19922, -792.946411, -292.354706, -0.998633981, 0.0214761049, -0.0476294532, -1.18918979e-05, 0.911520779, 0.41125378, 0.0522473752, 0.410692573, -0.910275519)
    end
})

-- Desolate Pocket
TeleportTab:CreateButton({
    Name = "Desolate Pocket",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1653.20789, -209.569794, -2826.66235, -0.75154984, -0.448706299, 0.483565092, -9.56760141e-06, 0.733041525, 0.680183828, -0.659676075, 0.511187434, -0.5509215)
    end
})

-- Harvesters Spike
TeleportTab:CreateButton({
    Name = "Harvesters Spike",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1294.44336, 239.924286, 1561.66492, 0.934017003, 0.279367268, -0.222634062, -1.35371874e-06, 0.623229206, 0.782039106, 0.357228249, -0.730437636, 0.582107008)
    end
})


-- Statue of Sovereignty
TeleportTab:CreateButton({
    Name = "Statue of Sovereignty",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3.59877586, 428.079468, -1120.38855, -0.744521737, 0.29356274, -0.599589884, -3.29937052e-06, 0.89812839, 0.439733088, 0.667598069, 0.327392787, -0.668675244)
    end
})

-- Haddock Rock
TeleportTab:CreateButton({
    Name = "Haddock Rock",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-606.347534, 212.824554, -465.768677, -0.960802555, -0.0826905817, 0.264613658, -3.89933166e-06, 0.954485118, 0.298258275, -0.277232975, 0.286566198, -0.917072177)
    end
})

-- Earmark Island
TeleportTab:CreateButton({
    Name = "Earmark Island",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1228.75549, 160.954803, 504.746521, 0.105785392, -0.125730574, 0.986408234, -9.6655226e-09, 0.991974235, 0.126440093, -0.994388938, -0.0133755207, 0.104936391)
    end
})

-- The Arch
TeleportTab:CreateButton({
    Name = "The Arch",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1052.06848, 321.8638, -1249.91492, -0.781760037, -0.174461573, 0.59867698, -3.93326582e-06, 0.960067034, 0.279769868, -0.623579144, 0.218710497, -0.75054276)
    end
})

TeleportTab:CreateButton({
    Name = "random spot in the ocean that is popular",
    Callback = function()
        local targetCFrame = CFrame.new(-805.568481, 140.161438, 1195.56104, -0.947355151, 0.150438279, -0.28264159, -3.21241237e-06, 0.882742167, 0.469857544, 0.320184261, 0.445122838, -0.836269915)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = targetCFrame
        local part = Instance.new("Part")
        part.Size = Vector3.new(10, 1, 10)
        part.CFrame = targetCFrame
        part.Anchored = true
        part.Parent = workspace
    end
})

local extrashitTab = Window:CreateTab("extra stuff", 4483362458)

extrashitTab:CreateButton({
    Name = "Infinite Yield",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
    end
})

extrashitTab:CreateButton({
    Name = "Remote Spy",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/infyiff/backup/main/SimpleSpyV3/main.lua"))()
    end
})

extrashitTab:CreateButton({
    Name = "Dex Explorer",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/infyiff/backup/main/dex.lua"))()
    end
})
