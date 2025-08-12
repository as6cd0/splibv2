# SP Library v2
This documentation is for SP Library
## Booting the Library
```lua
local splib = loadstring(game:HttpGet("https://raw.githubusercontent.com/as6cd0/SP_Hub/refs/heads/main/splibv2"))()
---
## Creating a Window

```lua
local Window = splib:MakeWindow({
 Name = "SP Library v2",
 HidePremium = false,
 SaveConfig = true,
 Setting = true,
 ToggleIcon = "rbxassetid://83114982417764",
 ConfigFolder = "SPHubConfigs",
 CloseCallback = true
})

--[[
Name = <string> - The name of the UI.
HidePremium = <bool> - Whether or not the user details shows Premium status or not.
SaveConfig = <bool> - Toggles the config saving in the UI.
Setting = <bool> - Toggle to show the setting on the window
ToggleIcon = <string> - URL to the image you want displayed on the toggle window.
ConfigFolder = <string> - The name of the folder where the configs are saved.
CloseCallback = <function> - Function to execute when the window is closed.
]]
