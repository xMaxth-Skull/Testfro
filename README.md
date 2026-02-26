-- [[ CONFIGURATION ]]
_G.AutoPickups = true          -- Automatically picks up rewards like snow charms
_G.AntiLag = false             -- Reduces graphical lag by unloading unnecessary elements
_G.ClaimRewards = true         -- Automatically claims daily rewards like spins

-- [[ WEBHOOK SETTINGS ]]
_G.SendWebhook = false         -- Set to true to enable notifications (via a webhook)
_G.Webhook = "YOUR-WEBHOOK-URL-HERE"

-- [[ LIBRARY INITIALIZATION ]]
local TDS = loadstring(game:HttpGet("https://raw.githubusercontent.com/raxs0420/test/refs/heads/main/library%20new/new%20ui%20test%20test.lua"))()

-- [[ LOBBY: Equip Loadout and Start the Game ]]
TDS:Loadout("Necromancer", "Scout", "Mercenary Base", "Hacker") -- Specify towers
TDS:Mode("Frost")                                               -- Set the game mode to "Frost"

-- [[ WAIT UNTIL IN-GAME ]]
-- GameInfo, Place, and Upgrade functions only work after the game starts
local player_gui = game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui")
repeat task.wait(1) until player_gui:FindFirstChild("ReactGameIntermission")

-- [[ VOTE MAP AND MODIFIERS ]]
TDS:GameInfo("Summer Castle", {})  -- Specify the map and any modifiers (currently empty)
TDS:AutoSkip("T")                  -- Automatically skips waves

-- [[ STRATEGY SCRIPT: Place and Upgrade Towers ]]
-- Place and upgrade towers based on your predefined strategy
macroURL = "https://
raw.githubusercontent.com/
yourname/macro.lua", -- Your raw
github macro link

-- Add more placements and upgrades if necessary
-- This section includes only a portion of your strategy for clarity
-- Continue adding your full strategy here

-- [[ OPTIONAL: RESTART GAME AFTER COMPLETION ]]
TDS:RestartGame() -- Automatically restart for farming strategies
