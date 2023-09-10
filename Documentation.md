# WallyV3 Library Documentation

## Introduction

This documentation serves as a comprehensive guide for the WallyV3 UI library. Please note, this library was not developed by me. All credits go to [this creator](https://v3rmillion.net/member.php?action=profile&uid=507120) on V3rmillion.

## Booting the Library

To start using the library's features, you need to boot it up first.

```lua
local WallyLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wall%20v3')))()
```


## Creating A Window
```lua
local Window = library:CreateWindow("Window")

--[[
Name = Window (Change "Window" To The Name Of Your Choice!)
--]]
```

## Making A Folder
```lua
local Folder = Window:CreateFolder("Folder")

--[[
Name = Folder (Chnage "Folder" To The Name Of Your Choice!)
--]]
```


## Making A Button
```lua
Folder:Button("Button", function()
    print("Clicked The Button!")
end)

--[[
Name = Button (Change "Button" to the name of your choice!)
Callback = function that runs when the button is clicked.
]]
```


## Making A Toggle
```lua
Folder:Toggle("Toggle", function(bool)
    shared.toggle = bool
    print(shared.toggle)
end)

--[[
Name = Toggle (Change "Toggle" to the name of your choice!)
Callback = function that runs when the toggle state changes.
]]
```


## Making A TextBox
```lua
Folder:Box("Textbox", "text", function(value)
    print(value)
end)

--[[
Name = Textbox (Change "Textbox" to the name of your choice!)
Type = The type of input ("number" or "string").
Callback = function that runs when text is entered.
]]
```


## Making A Dropdown
```lua
Folder:Dropdown("Dropdown", {"A", "B", "C"}, true, function(selectedOption)
    print(selectedOption)
end)

--[[
Name = Dropdown (Change "Dropdown" to the name of your choice!)
Options = The list of choices available in the dropdown.
Callback = function that runs when an option is selected.
]]
```


## Making A Slider
```lua
Folder:Slider("Slider", {
    min = 10; -- Minimum value of the slider
    max = 50; -- Maximum value of the slider
    precise = true; -- Use up to 2 decimal places
}, function(value)
    print(value)
end)

--[[
Name = Slider (Change "Slider" to the name of your choice!)
Callback = function that runs when the slider value changes.
]]
```


## Making A Label
```lua
Folder:Label("Text", {
    TextSize = 25; -- Size of the label text
    TextColor = Color3.fromRGB(255,255,255); -- Color of the label text
    BgColor = Color3.fromRGB(69,69,69); -- Background color of the label
})

--[[
Text = "Text" (Change the text to your desired label)
TextSize = Size of the label text
TextColor = Color of the label text
BgColor = Background color of the label
]]
```



## Making A Color Picker
```lua
Folder:ColorPicker("ColorPicker", Color3.fromRGB(255, 0, 0), function(color)
    print(color)
end)

--[[
Name = ColorPicker (Change "ColorPicker" to the name of your choice!)
Default = The default color when the color picker is first displayed.
Callback = function that runs when a color is selected.
]]
```



## Making A Bind
```lua
Folder:Bind("Bind", Enum.KeyCode.C, function()
    print("Key C was pressed!")
end)

--[[
Name = Bind (Change "Bind" to the name of your choice!)
Key = The default key for the bind.
Callback = function that runs when the assigned key is pressed.
]]
```

## Destory The Ui

```lua
Folder:DestroyGui()
```
