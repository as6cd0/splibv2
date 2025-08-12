# SP Library v2
This documentation is for SP Library
## Booting the Library
```lua
local splib = loadstring(game:HttpGet("https://raw.githubusercontent.com/as6cd0/SP_Hub/refs/heads/main/splibv2"))()
```




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
```

## Creating a Tab
```lua
local Tab = Window:MakeTab({
 IsMobile = false,
 IsPC = false,
	Name = "Tab 1",
	Icon = "rbxassetid://4483345998"
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
]]
```


## Creating a Section
```lua
local Section = Tab:AddSection({
	Name = "Section"
})

--[[
Name = <string> - The name of the section.
]]
```

## Create a Notification
```lua
splib:MakeNotification({
	Name = "Title",
	Content = "Hello",
	Image = "rbxassetid://6026568198",
	Time = 5
})

--[[
Title = <string> - The title of the notification.
Content = <string> - The content of the notification.
Image = <string> - The icon of the notification.
Time = <number> - The duration of the notfication.
]]
```
## Creating a Button
```lua
Tab:AddButton({
 IsMobile = false,
 IsPC = false,
	Name = "Button",
 Desc = "What is this button do?",
	Callback = function()
      		print("button pressed")
  	end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the button.
Desc = <string> - This is to write a description of what he's doing.
Callback = <function> - The function of the button.
]]
```

## Creating a Toggle
```lua
Tab:AddToggle({
 IsMobile = false,
 IsPC = false,
	Name = "Toggle",
 Desc = "What is this toggle do?",
	Default = false,
 Flag = "ToggleSave",
	Callback = function(Value)
		print(Value)
	end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the toggle.
Desc = <string> - This is to write a description of what he's doing.
Default = <bool> - The default value of the toggle.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the toggle.
]]
```


## Changing the value of an existing Toggle
```lua
Toggle:Set(true)
```

## Creating a Color Picker
```lua
Tab:AddColorpicker({
 IsMobile = false,
 IsPC = false,
	Name = "Colorpicker",
	Default = Color3.fromRGB(255, 0, 0),
 Flag = "ColorpickerSave",
	Callback = function(Value)
		print(Value)
	end	  
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the colorpicker.
Default = <color3> - The default value of the colorpicker.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the colorpicker.
]]
```

## Setting the color picker's value
```lua
ColorPicker:Set(Color3.fromRGB(255,255,255))
```

## Creating a Slider
```lua
Tab:AddSlider({
  IsMobile = false,
  IsPC = false,
  Name = "Slider",
  Min = 0,
  Max = 20,
  Increment = 1,
  Default = 10,
  ValueName = "string",
  Flag = "SliderSave",
  Callback = function(Value)
    print(Value)
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the slider.
Min = <number> - The minimal value of the slider.
Max = <number> - The maxium value of the slider.
Increment = <number> - How much the slider will change value when dragging.
Default = <number> - The default value of the slider.
ValueName = <string> - The text after the value number.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the slider.
]]
```
## Change Slider Value
```lua
Slider:Set(2)
```

## Creating a Label
```lua
Tab:AddLabel("Label")
```

## Changing the value of an existing label
```lua
Label:Set("Label Changed Value")
```

## Creating a Paragraph
```lua
Tab:AddParagraph("Paragraph","Paragraph Content")
```
## Changing an existing paragraph
```lua
CoolParagraph:Set("Paragraph New", "New Paragraph Content")
```

## Creating a TextBox
```lua
Tab:AddTextbox({
  IsMobile = false,
  IsPC = false,
  Name = "Textbox",
  Desc = "What is this textbox do?",
  Default = "default box input",
  TextDisappear = true,
  Flag = "textboxsave",
  Callback = function(Value)
    print(Value)
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the textbox.
Desc = <string> - This is to write a description of what he's doing.
Default = <string> - The default value of the textbox.
TextDisappear = <bool> - Makes the text disappear in the textbox after losing focus.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the textbox.
]]
```
## Creating a Keybind
```lua
Tab:AddBind({
  IsMobile = false,
  IsPC = false,
  Name = "Bind",
  Desc = "What is this bind do?",
  Default = Enum.KeyCode.E,
  Hold = false,
  Flag = "bindsave",
  Callback = function()
    print("pressWORLRLRLLL")
  end    
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the bind.
Desc = <string> - This is to write a description of what he's doing.
Default = <keycode> - The default value of the bind.
Hold = <bool> - Makes the bind work like: Holding the key > The bind returns true, Not holding the key > Bind returns false.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the bind.
]]
```
## Chaning the value of a bind
```lua
Bind:Set(Enum.KeyCode.E)
```


## Creating a Dropdown
```lua
Tab:AddDropdown({
  IsMobile = false,
  IsPC = false,
    Name = "Dropdown",
    Desc = "What is this dropdown do?",
    Default = "1",
    Options = {"1", "2", "3"},
    Flag = "dropdownsave",
    Callback = function(value)
        print(value)
    end
})

--[[
IsMobile = <bool> - This is if you want to view it on mobile only
IsPc = <bool> - This is if you want to view it on pc only
Name = <string> - The name of the dropdown.
Desc = <string> - This is to write a description of what he's doing.
Default = <string> - The default value of the dropdown.
Options = <table> - The options in the dropdown.
Flag <string> - This is if you want to save the value even after the library is closed.
Callback = <function> - The function of the dropdown.
]]
```
## Adding a set of new Dropdown buttons to an existing menu (Refresh a existing dropdown)
```lua
Dropdown:Refresh(List<table>,true)
```

## Selecting a dropdown option
```lua
Dropdown:Select("dropdown option")
```

## Set a value from a dropdown option
```lua
Dropdown:Set("dropdown option")
```

