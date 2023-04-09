for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.Idled)) do
    v:Disable()
end

getgenv().SecureMode = true
local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Rayfield/main/source'))()


Rayfield:Notify({
   Title = "Made by an idiot",
   Content = "-- https://discord.gg/ng2TJv7K8b, -- Last updated 9-4-2023 (EU) 4-9-2023 (UK,US)",
   Duration = 5,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "ok.",
         Callback = function()
      end
   },
},
})


local Window = Rayfield:CreateWindow({
   Name = "Infinite Rarities GUI [BETA 0.2]",
   LoadingTitle = "Infinite Rarities [BETA 0.2]",
   LoadingSubtitle = "made by an idiot",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Infinite Rarities"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD.
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "",
      Subtitle = "",
      Note = "",
      FileName = "",
      SaveKey = false,
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = ""
   }
})

local Tab = Window:CreateTab("Update-Log") -- Title
local Label = Tab:CreateLabel("Updates -- 9-4-2023 (EU) 4-9-2023 (UK,US)")
local Label = Tab:CreateLabel("Changed Teleports to be smoother, added more Teleports.")
local Label = Tab:CreateLabel("Added more auto-farms.")
local Label = Tab:CreateLabel("Made all buttons farm a bit faster.")
local Label = Tab:CreateLabel("Changed how NPC Farm works.")
local Label = Tab:CreateLabel("Added a built in anti afk.")




local Tab = Window:CreateTab("Auto-Farms") -- Title
local Label = Tab:CreateLabel("Button Farms")
local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm SP -- Sacrifice",
   CurrentValue = false,
   Flag = "SPFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(s)
    shared["SPFarm"] = s
    while shared["SPFarm"] do
      task.wait (0.1)
      if not shared["SPFarm"] then
          break
      end
     
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5331802, 3.09631896, 39.5371666, 0.999995887, -6.09746564e-08, -0.00286680576, 6.11561006e-08, 1, 6.32036929e-08, 0.00286680576, -6.33787565e-08, 0.999995887)
wait (0.6)
end
end
end
end,
})



local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm PP -- Prestige",
   CurrentValue = false,
   Flag = "PPFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(p)
    shared["PPFarm"] = p
    while shared["PPFarm"] do
      task.wait (0.1)
      if not shared["PPFarm"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 9 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 9 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5177002, 3.09631896, -40.5800743, 0.999967277, 7.1605113e-09, -0.00809009559, -6.64147226e-09, 1, 6.41842064e-08, 0.00809009559, -6.41283719e-08, 0.999967277)
wait (0.6)
end
end
end
end,
})



local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm AP -- Ascend",
   CurrentValue = false,
   Flag = "APFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(a)
    shared["APFarm"] = a
    while shared["APFarm"] do
      task.wait (0.1)
      if not shared["APFarm"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 23 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 23 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-40.4744759, 3.09631896, -40.5869484, 0.999985874, -4.0322039e-08, -0.00531473942, 4.05476683e-08, 1, 4.23456576e-08, 0.00531473942, -4.25605613e-08, 0.999985874)
wait (0.6)
end
end
end
end,
})



local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm TP -- Trancend",
   CurrentValue = false,
   Flag = "TPFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(a)
    shared["TPFarm"] = a
    while shared["TPFarm"] do
      task.wait (0.1)
      if not shared["TPFarm"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 104 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 104 then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.792343, 16.3463192, 18.0036583, 0.999923408, 2.5762299e-08, -0.0123764426, -2.5598812e-08, 1, 1.3368032e-08, 0.0123764426, -1.30501858e-08, 0.999923408)
wait (0.6)
end
end
end
end,
})



local Toggle = Tab:CreateToggle({
    
    Name = "Autofarm RP -- Rebirth",
    CurrentValue = false,
    Flag = "RPFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
    Callback = function(RP)
     shared["RPFarm"] = RP
     while shared["RPFarm"] do
       task.wait (0.1)
       if not shared["RPFarm"] then
           break
          end
          if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 3 then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5331802, 3.09631896, 39.5371666, 0.999995887, -6.09746564e-08, -0.00286680576, 6.11561006e-08, 1, 6.32036929e-08, 0.00286680576, -6.33787565e-08, 0.999995887)
            wait (0.2)
          else
          if game:GetService("Players").LocalPlayer.PlayerData.HighestQuality.Value < 4 then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-74.0643387, 16.3463192, 59.7393723, -0.0104634259, 8.23616375e-09, 0.999945283, 5.95974541e-08, 1, -7.61298757e-09, -0.999945283, 5.95145337e-08, -0.0104634259)
        wait (1)
        else if game:GetService("Players").LocalPlayer.PlayerData.HighestQuality.Value >= 4 then
             game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.099915, 16.3463192, 69.5189285, 0.99999851, 6.06647577e-09, 0.00173973863, -6.04764994e-09, 1, -1.0826283e-08, -0.00173973863, 1.08157447e-08, 0.99999851)
        wait (0.6)
 end
 end
 end
 end
 end,
 })

local Label = Tab:CreateLabel("NPC Farm")
local Toggle = Tab:CreateToggle({
    
   Name = "NPC Autofarm",
   CurrentValue = false,
   Flag = "NPCFarm", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(n)
    shared["NPCFarm"] = n
    while shared["NPCFarm"] do
      task.wait (0.1)
      if not shared["NPCFarm"] then
          break
      end
     wait (0.1)
     if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 7 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
    else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 7 then
        wait (0.1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(66.3481522, 3.09631896, -4.49667692, -0.00352633093, 7.64874173e-08, -0.999993801, 3.38367521e-08, 1, 7.63685719e-08, 0.999993801, -3.35672432e-08, -0.00352633093)
        wait (0.25)
local player = game.Players.LocalPlayer.Character
local part = game:GetService("Workspace").PVPIsland.NPCs[" "].HumanoidRootPart
player.HumanoidRootPart.CFrame = part.CFrame
if game:GetService("Workspace").PVPIsland.NPCs[" "].Humanoid.Health == 0 then
    local part = game:GetService("Workspace").PVPIsland.NPCs[" "].HumanoidRootPart
    HumanoidRootPart:destroy()
    else
    wait (0.1)
    local player = game.Players.LocalPlayer.Character
local part = game:GetService("Workspace").PVPIsland.NPCs[" "].HumanoidRootPart
player.HumanoidRootPart.CFrame = part.CFrame
end
wait (5)
end
end
end
end,
})

local Label = Tab:CreateLabel("All Buttons Autofarm")

local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm All SP Buttons",
   CurrentValue = false,
   Flag = "ABFP", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(a)
    shared["ABFP"] = a
    while shared["ABFP"] do
      task.wait (0.1)
      if not shared["ABFP"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 3 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5331802, 3.09631896, 39.5371666, 0.999995887, -6.09746564e-08, -0.00286680576, 6.11561006e-08, 1, 6.32036929e-08, 0.00286680576, -6.33787565e-08, 0.999995887)
    wait (0.2)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5141106, 3.09631896, 27.4077129, 0.999908984, 5.37676108e-08, -0.0134895854, -5.34106874e-08, 1, 2.68195564e-08, 0.0134895854, -2.60966289e-08, 0.999908984)
    wait (0.15)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5177422, 3.09631896, 19.4198952, 0.999967515, 7.35386596e-09, -0.00805685204, -6.79004453e-09, 1, 7.00077365e-08, 0.00805685204, -6.99507581e-08, 0.999967515)
    wait (0.15)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5247688, 3.09631896, 11.4121437, 0.999977112, 3.20063892e-10, -0.00676661264, -3.30863781e-10, 1, -1.59493574e-09, 0.00676661264, 1.59713809e-09, 0.999977112)
    wait (0.15)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5252686, 3.09631896, 3.4133749, 0.999978185, -2.17039613e-08, -0.0066021001, 2.22197816e-08, 1, 7.80563312e-08, 0.0066021001, -7.82013316e-08, 0.999978185)
    wait (0.15)
end
end
end
end,
})

local Toggle = Tab:CreateToggle({
    
   Name = "Autofarm All PP Buttons",
   CurrentValue = false,
   Flag = "ABFPP", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(a)
    shared["ABFPP"] = a
    while shared["ABFPP"] do
      task.wait (0.1)
      if not shared["ABFPP"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 9 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 9 then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5177002, 3.09631896, -40.5800743, 0.999967277, 7.1605113e-09, -0.00809009559, -6.64147226e-09, 1, 6.41842064e-08, 0.00809009559, -6.41283719e-08, 0.999967277)
wait (0.2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(27.5251942, 3.09631896, -40.5863571, 0.999978006, -5.78475801e-09, -0.00662795315, 5.91668625e-09, 1, 1.98852064e-08, 0.00662795315, -1.99239842e-08, 0.999978006)
wait (0.15)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(19.5248928, 3.09631896, -40.5894623, 0.999986887, 6.21075245e-08, -0.0051263487, -6.2422707e-08, 1, -6.13233198e-08, 0.0051263487, 6.16425098e-08, 0.999986887)
wait (0.15)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(11.5254002, 3.09631896, -40.5867767, 0.999985933, 5.49936452e-08, -0.00530138612, -5.52921904e-08, 1, -5.61681404e-08, 0.00530138612, 5.64604754e-08, 0.999985933)
wait (0.15)
end
end
end
end,
})

local Toggle = Tab:CreateToggle({

   Name = "Autofarm All AP Buttons",
   CurrentValue = false,
   Flag = "ABFPA", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(a)
    shared["ABFPA"] = a
    while shared["ABFPA"] do
      task.wait (0.1)
      if not shared["ABFPA"] then
          break
         end
if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 23 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
wait (1)
else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 23 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-40.4744759, 3.09631896, -40.5869484, 0.999985874, -4.0322039e-08, -0.00531473942, 4.05476683e-08, 1, 4.23456576e-08, 0.00531473942, -4.25605613e-08, 0.999985874)
wait (0.2)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.5532303, 16.3463192, -17.8174248, 0.999888182, 6.60651445e-09, -0.01495477, -7.77297782e-09, 1, -7.79412659e-08, 0.01495477, 7.80487923e-08, 0.999888182)
wait (0.15)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.6719971, 16.3463192, -10.1226463, 0.999877691, -1.51108424e-08, -0.0156394113, 1.51858437e-08, 1, 4.6769757e-09, 0.0156394113, -4.91390129e-09, 0.999877691)
wait (0.15)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.75, 16.3463192, -2.16041446, 0.999999762, 1.81869098e-08, 0.00065232598, -1.82274533e-08, 1, 6.21443945e-08, -0.00065232598, -6.21562677e-08, 0.999999762)
wait (0.15)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.7641983, 16.3463192, 6.02441835, 0.999418497, 1.60401683e-08, 0.0340973586, -1.72173706e-08, 1, 3.42311246e-08, -0.0340973586, -3.47982869e-08, 0.999418497)
wait (0.15)
end
end
end
end,
})

local Toggle = Tab:CreateToggle({

    Name = "Autofarm All TP Buttons",
    CurrentValue = false,
    Flag = "ABFPT", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
    Callback = function(TP)
     shared["ABFPT"] = TP
     while shared["ABFPT"] do
       task.wait (0.1)
       if not shared["ABFPT"] then
           break
          end
 if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value < 104 then
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
 wait (1)
 else if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 104 then
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.792343, 16.3463192, 18.0036583, 0.999923408, 2.5762299e-08, -0.0123764426, -2.5598812e-08, 1, 1.3368032e-08, 0.0123764426, -1.30501858e-08, 0.999923408)
 wait (0.2)
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.79425, 16.3463192, 38.0096588, 0.999950886, 3.39233139e-08, -0.00991246384, -3.49822962e-08, 1, -1.06660266e-07, 0.00991246384, 1.07001782e-07, 0.999950886)
 wait (0.15)
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-136.792862, 16.3463192, 38.0048332, 0.999920785, 1.52681565e-08, -0.0125884796, -1.5202783e-08, 1, 5.28870636e-09, 0.0125884796, -5.09690734e-09, 0.999920785)
 wait (0.15)
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-128.595169, 16.3463192, 38.1105499, 0.999876499, 5.23073176e-08, -0.015715735, -5.27019743e-08, 1, -2.46980392e-08, 0.015715735, 2.55232386e-08, 0.999876499)
 wait (0.15)
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-120.705551, 16.3463192, 38.1770744, 0.999961853, 4.80839084e-11, -0.0087334495, -4.82814899e-11, 1, -2.24127921e-11, 0.0087334495, 2.28336013e-11, 0.999961853)
 wait (0.15)
 end
 end
 end
 end,
 })

 local Toggle = Tab:CreateToggle({

    Name = "Autofarm All RP Buttons",
    CurrentValue = false,
    Flag = "ABFPR", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
    Callback = function(TP)
     shared["ABFPR"] = TP
     while shared["ABFPR"] do
       task.wait (0.1)
       if not shared["ABFPR"] then
           break
          end
          if game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value >= 3 then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5331802, 3.09631896, 39.5371666, 0.999995887, -6.09746564e-08, -0.00286680576, 6.11561006e-08, 1, 6.32036929e-08, 0.00286680576, -6.33787565e-08, 0.999995887)
            wait (0.2)
          else
          if game:GetService("Players").LocalPlayer.PlayerData.HighestQuality.Value < 4 then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-74.0643387, 16.3463192, 59.7393723, -0.0104634259, 8.23616375e-09, 0.999945283, 5.95974541e-08, 1, -7.61298757e-09, -0.999945283, 5.95145337e-08, -0.0104634259)
        wait (1)
        else if game:GetService("Players").LocalPlayer.PlayerData.HighestQuality.Value >= 4 then
             game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.099915, 16.3463192, 69.5189285, 0.99999851, 6.06647577e-09, 0.00173973863, -6.04764994e-09, 1, -1.0826283e-08, -0.00173973863, 1.08157447e-08, 0.99999851)
        wait (0.2)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-127.475616, 16.3463192, 69.8512878, 0.999945045, 1.62998077e-08, -0.0104820738, -1.6534992e-08, 1, -2.23502621e-08, 0.0104820738, 2.25223555e-08, 0.999945045)
        wait (0.15)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-120.014389, 16.3463192, 69.9034195, 0.999975562, 2.26749215e-08, -0.0069908672, -2.28746941e-08, 1, -2.849632e-08, 0.0069908672, 2.86555366e-08, 0.999975562)
        wait (0.15)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-113.166428, 16.3463192, 69.9871063, 0.999925256, 9.23025123e-09, -0.0122258598, -9.38629618e-09, 1, -1.27060842e-08, 0.0122258598, 1.281989e-08, 0.999925256)
        wait (0.15)
 end
 end
 end
 end
 end,
 })




local Tab = Window:CreateTab("Player") -- Title
local Label = Tab:CreateLabel("LocalPlayer")

local Button = Tab:CreateButton({
   Name = "CFrame Walkspeed",
   Callback = function()
      local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';
UIS.InputBegan:connect(function(UserInput)
        if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.W then
            _G.Running = true
                while wait(0.005) and _G.Running == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 0.05
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 0.05
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 0.05
end
        end
end)
UIS.InputEnded:connect(function(UserInput)
        if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.W then
                _G.Running = false
        end
end)
   end,
})

local Label = Tab:CreateLabel("Miscs")
local Button = Tab:CreateButton({
    
   Name = "Infinite Jump",
   Callback = function(I)
local InfJump = true
game:GetService("UserInputService").jumpRequest:Connect(function()
    if InfJump then
        game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass"Humanoid":ChangeState("Jumping")
    end
end)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "Server Lagger -- Press M",
   Callback = function(l)
      local isScriptEnabled = false
local toggleKey = Enum.KeyCode.M

local function getmaxvalue(val)
    local mainvalueifonetable = 499999
    if type(val) ~= "number" then
        return nil
    end
    local calculateperfectval = (mainvalueifonetable/(val+2))
    return calculateperfectval
end

local function bomb(tableincrease, tries)
    local maintable = {}
    local spammedtable = {}

    table.insert(spammedtable, {})
    z = spammedtable[1]

    for i = 1, tableincrease do
        local tableins = {}
        table.insert(z, tableins)
        z = tableins
    end

    local calculatemax = getmaxvalue(tableincrease)
    local maximum

    if calculatemax then
        maximum = calculatemax
    else
        maximum = 1999999
    end

    for i = 1, maximum do
        table.insert(maintable, spammedtable)
    end

    for i = 1, tries do
        game.RobloxReplicatedStorage.SetPlayerBlockList:FireServer(maintable)
    end
end

local function toggleScript(input, gameProcessedEvent)
    if input.KeyCode == toggleKey and not gameProcessedEvent then
        isScriptEnabled = not isScriptEnabled
        if isScriptEnabled then
            print("Lagger ON")
        else
            print("Lagger OFF")
        end
    end
end

game:GetService("UserInputService").InputBegan:Connect(toggleScript)

while true do
    if isScriptEnabled then
        game:GetService("NetworkClient"):SetOutgoingKBPSLimit(math.huge)
        bomb(2, 2) --// change values if client crashes
    end
    wait(0.6)
end 
end,
})

local Label = Tab:CreateLabel("Expansions (client sided, unless you have them unlocked)")
local Button = Tab:CreateButton({
    
   Name = "PVP Expansion",
   Callback = function(I)
local object = game.ReplicatedStorage.PVPExpansion:Clone()
object.Parent = game.Workspace
   end,
})

local Button = Tab:CreateButton({
    
   Name = "APMap Expansion",
   Callback = function(I)
local object = game.ReplicatedStorage.APMapExpansion:Clone()
object.Parent = game.Workspace
   end,
})

local Button = Tab:CreateButton({
    
   Name = "APMapExpansion2",
   Callback = function(I)
local object = game.ReplicatedStorage.APMapExpansion2:Clone()
object.Parent = game.Workspace
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TPMapEpansion",
   Callback = function(I)
local object = game.ReplicatedStorage.TPMapExpansion:Clone()
object.Parent = game.Workspace
   end,
})


local Label = Tab:CreateLabel("Server-Hop")
local Button = Tab:CreateButton({
    
   Name = "Server Hop",
   Callback = function(c)
      local PlaceID = 12802235086
local AllIDs = {}
local foundAnything = ""
local actualHour = os.date("!*t").hour
local Deleted = false
local File = pcall(function()
    AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
end)
if not File then
    table.insert(AllIDs, actualHour)
    writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
end
function TPReturner()
    local Site;
    if foundAnything == "" then
        Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
    else
        Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
    end
    local ID = ""
    if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
        foundAnything = Site.nextPageCursor
    end
    local num = 0;
    for i,v in pairs(Site.data) do
        local Possible = true
        ID = tostring(v.id)
        if tonumber(v.maxPlayers) > tonumber(v.playing) then
            for _,Existing in pairs(AllIDs) do
                if num ~= 0 then
                    if ID == tostring(Existing) then
                        Possible = false
                    end
                else
                    if tonumber(actualHour) ~= tonumber(Existing) then
                        local delFile = pcall(function()
                            delfile("NotSameServers.json")
                            AllIDs = {}
                            table.insert(AllIDs, actualHour)
                        end)
                    end
                end
                num = num + 1
            end
            if Possible == true then
                table.insert(AllIDs, ID)
                wait()
                pcall(function()
                    writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                    wait()
                    game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                end)
                wait(4)
            end
        end
    end
end

function Teleport()
    while wait() do
        pcall(function()
            TPReturner()
            if foundAnything ~= "" then
                TPReturner()
            end
        end)
    end
end


Teleport()
end,
})

local Tab = Window:CreateTab("Teleports") -- Title
local Label = Tab:CreateLabel("Rarities")

local Button = Tab:CreateButton({
    
   Name = "RarityGet",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0.0251196921, 3.09631896, 39.9141159, 0.999977827, 1.3908239e-08, -0.00665492332, -1.41655976e-08, 1, -3.86247336e-08, 0.00665492332, 3.87181522e-08, 0.999977827)
   end,
})

local Button = Tab:CreateButton({
    
    Name = "QualityGet",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-74.0643387, 16.3463192, 59.7393723, -0.0104634259, 8.23616375e-09, 0.999945283, 5.95974541e-08, 1, -7.61298757e-09, -0.999945283, 5.95145337e-08, -0.0104634259)
    end,
 })

local Label = Tab:CreateLabel("SP Buttons")

local Button = Tab:CreateButton({
    
   Name = "Sacrifice",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5331802, 3.09631896, 39.5371666, 0.999995887, -6.09746564e-08, -0.00286680576, 6.11561006e-08, 1, 6.32036929e-08, 0.00286680576, -6.33787565e-08, 0.999995887)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "SP Luck",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5141106, 3.09631896, 27.4077129, 0.999908984, 5.37676108e-08, -0.0134895854, -5.34106874e-08, 1, 2.68195564e-08, 0.0134895854, -2.60966289e-08, 0.999908984)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "Roll Cooldown",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5177422, 3.09631896, 19.4198952, 0.999967515, 7.35386596e-09, -0.00805685204, -6.79004453e-09, 1, 7.00077365e-08, 0.00805685204, -6.99507581e-08, 0.999967515)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "Bulk Roll",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5247688, 3.09631896, 11.4121437, 0.999977112, 3.20063892e-10, -0.00676661264, -3.30863781e-10, 1, -1.59493574e-09, 0.00676661264, 1.59713809e-09, 0.999977112)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "SP Multiplier",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5252686, 3.09631896, 3.4133749, 0.999978185, -2.17039613e-08, -0.0066021001, 2.22197816e-08, 1, 7.80563312e-08, 0.0066021001, -7.82013316e-08, 0.999978185)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "SP - PVP Expansion",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5245476, 3.09631896, -4.5889225, 0.999976575, -5.74149173e-09, -0.00684721163, 6.07701756e-09, 1, 4.89810539e-08, 0.00684721163, -4.90215193e-08, 0.999976575)
end,
})

local Label = Tab:CreateLabel("PP Buttons")

local Button = Tab:CreateButton({
    
   Name = "Prestige",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(39.5177002, 3.09631896, -40.5800743, 0.999967277, 7.1605113e-09, -0.00809009559, -6.64147226e-09, 1, 6.41842064e-08, 0.00809009559, -6.41283719e-08, 0.999967277)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "PP Luck",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(27.5251942, 3.09631896, -40.5863571, 0.999978006, -5.78475801e-09, -0.00662795315, 5.91668625e-09, 1, 1.98852064e-08, 0.00662795315, -1.99239842e-08, 0.999978006)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "PP SP Multiplier",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(19.5248928, 3.09631896, -40.5894623, 0.999986887, 6.21075245e-08, -0.0051263487, -6.2422707e-08, 1, -6.13233198e-08, 0.0051263487, 6.16425098e-08, 0.999986887)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "PP PP Multiplier",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(11.5254002, 3.09631896, -40.5867767, 0.999985933, 5.49936452e-08, -0.00530138612, -5.52921904e-08, 1, -5.61681404e-08, 0.00530138612, 5.64604754e-08, 0.999985933)
   end,
})

local Label = Tab:CreateLabel("AP Buttons")

local Button = Tab:CreateButton({
    
   Name = "Ascend",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-40.4744759, 3.09631896, -40.5869484, 0.999985874, -4.0322039e-08, -0.00531473942, 4.05476683e-08, 1, 4.23456576e-08, 0.00531473942, -4.25605613e-08, 0.999985874)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.7641983, 16.3463192, 6.02441835, 0.999418497, 1.60401683e-08, 0.0340973586, -1.72173706e-08, 1, 3.42311246e-08, -0.0340973586, -3.47982869e-08, 0.999418497)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP PP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.75, 16.3463192, -2.16041446, 0.999999762, 1.81869098e-08, 0.00065232598, -1.82274533e-08, 1, 6.21443945e-08, -0.00065232598, -6.21562677e-08, 0.999999762)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP SP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.6719971, 16.3463192, -10.1226463, 0.999877691, -1.51108424e-08, -0.0156394113, 1.51858437e-08, 1, 4.6769757e-09, 0.0156394113, -4.91390129e-09, 0.999877691)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP Luck",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-92.5532303, 16.3463192, -17.8174248, 0.999888182, 6.60651445e-09, -0.01495477, -7.77297782e-09, 1, -7.79412659e-08, 0.01495477, 7.80487923e-08, 0.999888182)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP Map Expansion",
   Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-40.4821091, 3.09631896, -28.5804405, 0.999977589, 2.21834888e-08, -0.00669103255, -2.26509425e-08, 1, -6.97869993e-08, 0.00669103255, 6.99369949e-08, 0.999977589)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "AP Map Expansion 2",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-84.6445618, 16.3463192, 6.28656244, 0.999988317, -6.24680219e-09, -0.00483552227, 5.77227999e-09, 1, -9.81465078e-08, 0.00483552227, 9.81174537e-08, 0.999988317)
   end,
})

local Label = Tab:CreateLabel("TP Buttons")

local Button = Tab:CreateButton({
    
   Name = "Trancend",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.792343, 16.3463192, 18.0036583, 0.999923408, 2.5762299e-08, -0.0123764426, -2.5598812e-08, 1, 1.3368032e-08, 0.0123764426, -1.30501858e-08, 0.999923408)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TP AP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.79425, 16.3463192, 38.0096588, 0.999950886, 3.39233139e-08, -0.00991246384, -3.49822962e-08, 1, -1.06660266e-07, 0.00991246384, 1.07001782e-07, 0.999950886)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TP PP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-136.792862, 16.3463192, 38.0048332, 0.999920785, 1.52681565e-08, -0.0125884796, -1.5202783e-08, 1, 5.28870636e-09, 0.0125884796, -5.09690734e-09, 0.999920785)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TP SP Multiplier",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-128.595169, 16.3463192, 38.1105499, 0.999876499, 5.23073176e-08, -0.015715735, -5.27019743e-08, 1, -2.46980392e-08, 0.015715735, 2.55232386e-08, 0.999876499)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TP Luck",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-120.705551, 16.3463192, 38.1770744, 0.999961853, 4.80839084e-11, -0.0087334495, -4.82814899e-11, 1, -2.24127921e-11, 0.0087334495, 2.28336013e-11, 0.999961853)
   end,
})

local Button = Tab:CreateButton({
    
   Name = "TP Super Upgrade",
   Callback = function(TP)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-132.694519, 16.3463192, 18.1093445, 0.999961853, 2.73184018e-08, -0.00873669703, -2.65736624e-08, 1, 8.53588631e-08, 0.00873669703, -8.5123439e-08, 0.999961853)
   end,
})

local Button = Tab:CreateButton({
    
    Name = "TP Map Expansion",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-88.8228531, 16.3463192, 38.4343452, 0.999847651, 1.63848366e-08, -0.0174547993, -1.65898193e-08, 1, -1.15988392e-08, 0.0174547993, 1.18866437e-08, 0.999847651)
    end,
 })

 local Label = Tab:CreateLabel("RP Buttons")

 local Button = Tab:CreateButton({
    
    Name = "Rebirth",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-144.099915, 16.3463192, 69.5189285, 0.99999851, 6.06647577e-09, 0.00173973863, -6.04764994e-09, 1, -1.0826283e-08, -0.00173973863, 1.08157447e-08, 0.99999851)
    end,
 })

 local Button = Tab:CreateButton({
    
    Name = "RP Super Upgrade",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-134.631958, 16.3463192, 69.6697388, 0.99984771, 3.33005872e-08, -0.01745308, -3.41040227e-08, 1, -4.57365239e-08, 0.01745308, 4.63247751e-08, 0.99984771)
    end,
 })

 local Button = Tab:CreateButton({
    
    Name = "Quality Bulk Roll",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-127.475616, 16.3463192, 69.8512878, 0.999945045, 1.62998077e-08, -0.0104820738, -1.6534992e-08, 1, -2.23502621e-08, 0.0104820738, 2.25223555e-08, 0.999945045)
    end,
 })

 local Button = Tab:CreateButton({
    
    Name = "Quality Roll Cooldown",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-120.014389, 16.3463192, 69.9034195, 0.999975562, 2.26749215e-08, -0.0069908672, -2.28746941e-08, 1, -2.849632e-08, 0.0069908672, 2.86555366e-08, 0.999975562)
    end,
 })


 local Button = Tab:CreateButton({
    
    Name = "Quality Luck",
    Callback = function(TP)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-113.166428, 16.3463192, 69.9871063, 0.999925256, 9.23025123e-09, -0.0122258598, -9.38629618e-09, 1, -1.27060842e-08, 0.0122258598, 1.281989e-08, 0.999925256)
    end,
 })




local Tab = Window:CreateTab("Player-Info") -- Title
local Label = Tab:CreateLabel("Player-Main Stats:")
local LabelHRarity = Tab:CreateLabel("-----")
local LabelHQuality = Tab:CreateLabel("-----")
      _G.PSR = true
      while _G.PSR == true do
      wait (0.25)
      HR = game:GetService("Players").LocalPlayer.PlayerData.HighestRarity.Value
      LabelHRarity:Set ("Rarity: #" .. HR)
      wait (0.25)
      HQ = game:GetService("Players").LocalPlayer.PlayerData.HighestQuality.Value
      LabelHQuality:Set ("Quality: #" .. HQ)
end


Rayfield:LoadConfiguration()
