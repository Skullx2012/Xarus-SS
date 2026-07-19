# Script
```lua
--[[
__   __                       _____ _____          __    __     _______               ______      _      __  
\ \ / /                      /  ___/  ___|        /  |  /  |   / / ___ \              | ___ \    | |     \ \ 
 \ V /  __ _ _ __ _   _ ___  \ `--.\ `--.  __   __`| |  `| |  | || |_/ / __ ___ ______| |_/ / ___| |_ __ _| |
 /   \ / _` | '__| | | / __|  `--. \`--. \ \ \ / / | |   | |  | ||  __/ '__/ _ \______| ___ \/ _ \ __/ _` | |
/ /^\ \ (_| | |  | |_| \__ \ /\__/ /\__/ /  \ V / _| |___| |_ | || |  | | |  __/      | |_/ /  __/ || (_| | |
\/   \/\__,_|_|   \__,_|___/ \____/\____/    \_(_)\___(_)___/ | |\_|  |_|  \___|      \____/ \___|\__\__,_| |
                                                               \_\                                       /_/ 
                                                                                                             
 _   _     _       _       _            _   _                                  _                             
| | | |   (_)     (_)     | |          | | (_)                                (_)                            
| |_| |__  _ ___   _ ___  | |_ ___  ___| |_ _ _ __   __ _  __   _____ _ __ ___ _  ___  _ __                  
| __| '_ \| / __| | / __| | __/ _ \/ __| __| | '_ \ / _` | \ \ / / _ \ '__/ __| |/ _ \| '_ \                 
| |_| | | | \__ \ | \__ \ | ||  __/\__ \ |_| | | | | (_| |  \ V /  __/ |  \__ \ | (_) | | | |                
 \__|_| |_|_|___/ |_|___/  \__\___||___/\__|_|_| |_|\__, |   \_/ \___|_|  |___/_|\___/|_| |_|                
                                                     __/ |                                                   
                                                    |___/          
]]--

local function webImport(file)
    return loadstring(game:HttpGetAsync(("https://raw.githubusercontent.com/NikSavchenko3/Xarus-SS/main/XarusSS.lua"):format(owner, branch, file)), file .. '.lua')()
end
```
# Xarus SS
Xarus SS - this is free server side executor.
<p align="center">
    <img src="https://media.discordapp.net/attachments/740850328316149760/877629799789629490/xss.png"/>
    </br>
    <a href="https://github.com/NikSavchenko3/Xarus-SS/releases">
    <img src="https://img.shields.io/github/downloads/NikSavchenko3/Xarus-SS/total?style=for-the-badge">
    <a href="https://github.com/NikSavchenko3/Xarus-SS/releases/tag/v.1.1">
    <img src="https://img.shields.io/github/v/release/NikSavchenko3/Xarus-SS.svg?include_prereleases&style=for-the-badge">
  </a>
    </br>
    <img src="https://media.discordapp.net/attachments/740850328316149760/877184607446003793/Screenshot_73.png" width="500px"/>
</p>

# What's new!
* Added 2 buttons!
  * Hide Button and Rejoin Button.
* Added Effect Buttons!
  * This is not bad effect. 
* Added FPS Counter!
  * This is not bad FPS Counter.

## Images/Videos 
<p><img align="center" alt="gif" src="https://imgur.com/a/gyXH2v0" width="300" height="300" /></p>
_sorry time out_
-- My Custom Executor by kid_n00b
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

local Frame = Instance.new("Frame")
Frame.Size = UDim2.new(0, 300, 0, 400)
Frame.Position = UDim2.new(0.5, -150, 0.5, -200)
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.Parent = ScreenGui

local Title = Instance.new("TextLabel")
Title.Text = "Xander Executor"
Title.Size = UDim2.new(1, 0, 0, 50)
Title.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
Title.Parent = Frame

local TextBox = Instance.new("TextBox")
TextBox.PlaceholderText = "Paste script here..."
TextBox.Size = UDim2.new(1, 0, 0, 200)
TextBox.Position = UDim2.new(0, 0, 0, 50)
TextBox.Parent = Frame

local ExecuteBtn = Instance.new("TextButton")
ExecuteBtn.Text = "Execute"
ExecuteBtn.Size = UDim2.new(0.5, 0, 0, 50)
ExecuteBtn.Position = UDim2.new(0, 0, 0, 250)
ExecuteBtn.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
ExecuteBtn.Parent = Frame
ExecuteBtn.MouseButton1Click:Connect(function()
    loadstring(TextBox.Text)()
end)

print("Xander Executor Loaded")