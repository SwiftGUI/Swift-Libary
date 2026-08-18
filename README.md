# Swift-Libary

> Swift is a modern and customizable Roblox UI Library.

![Swift Preview](https://cdn.discordapp.com/attachments/1533507488878432416/1539309484621434880/Sigma_Banner.png?ex=6a85d92c&is=6a8487ac&hm=46e3635ea056c0e5edb5c736368c634ecbdcf6d33ce2f40abaa3d7c1654e7789&)

**You can customize everything in Swift! We place a strong emphasis on making Swift Library beginner-friendly and easy to use.**

# Swift Features

- **Custom Themes**
- **Multiple GUI Styles**
- **Custom Fonts**
- **Custom Colors**
- **Default Themes**
- **Custom Loading Screen**

---

## How to Setup the Library

```lua
local SwiftUi = loadstring(game:HttpGet("https://api.getvortex.vip/api/t/QUGYKH/s/OfficialSwiftLib"))()
```

## Example
```lua
local SwiftUi = loadstring(game:HttpGet("https://api.getvortex.vip/api/t/QUGYKH/s/OfficialSwiftLib"))() 

local Window = SwiftUi:MakeWindow({
    Name = "Swift UI - Example Menu", --Example Name
    IntroEnabled = true, -- set the intro true or false 
    IntroText = "Swift Ui is Loading", -- intro text (if IntroEnabled = false you can delete this line)
    IntroIcon = "rbxassetid://123456",  -- intro icon (if IntroEnabled = false you can delete this line)
    SaveConfig = true, -- save settings if true than it saved or false than is doesnt save
    ConfigFolder = "TestConfigs", -- Config Folder name
    ConfigFileName = "Settings.json", -- Config File Name (in the Folder)
    ShowLoadNotification = false, -- shows the load notification
}) 

SwiftUi:MakeNotification({
    Name = "Example Name",
    Content = "Example Content",
    Time = 3 --custom time how long the notification should be shown
})

local ExampleTab = Window:MakeTab({
    Name = "Example Tab", -- Tab Name
    Icon = "rbxassetid://4483345998", --the icon for the Tab
})

ExampleTab:AddSection({
    Name = "Example Section" --Section Name
}) 

ExampleTab:AddColorpicker({
    Name = "Example Colorpicker",
    Default = Color3.fromRGB(255, 0, 0),
    Callback = function(Value)
        highlightColor = Value
        print("Ausgewählte Farbe:", Value)
    end
})

ExampleTab:AddButton({
    Name = "Example Button",
    Callback = function()
        print("Test Button Clicked")
    end
})

ExampleTab:AddToggle({
    Name = "ExampleToggle",
    Default = false,
    Callback = function(Value)
        print("Test Toggle Value: " .. tostring(Value))
    end
})

ExampleTab:AddSlider({
    Name = "Example Slider",
    Min = 0,
    Max = 100,
    Default = 50,
    Increment = 1,
    Callback = function(Value)
        print("Test Slider Value: " .. tostring(Value))
    end
})

ExampleTab:AddDropdown({
    Name = "Example Dropdown",
    Options = {"Option 1", "Option 2", "Option 3"},
    Default = "Option 1",
    Callback = function(Value)
        print("Test Dropdown Value: " .. Value)
    end
})

ExampleTab:AddTextbox({
    Name = "Example Textbox",
    Default = "", --if you dont write anything in it its nothing (empty)
    TextDisappear = true, --if you click enter after you typed the word or anythinf the text disappear (only if its true)
    Callback = function(Value)
        print("Test Textbox Value: " .. Value)
    end
})

ExampleTab:AddBind({
    Name = "Example Keybind",
    Default = Enum.KeyCode.RightShift,
    Callback = function()
        print("Test Keybind Pressed")
    end
})

ExampleTab:AddLabel("Example Label") --Label Text

ExampleTab:AddParagraph("Example Paragraph", "This is an example paragraph. You can add more text here to provide information or instructions.") --Paragraph Title and Text
```

## How to setup the individual features

### Window

```lua
local Window = SwiftUI:MakeWindow({
    Name = "Swift UI - Main", --Example Name
    IntroEnabled = true,
    IntroText = "Swift Ui is Loading",
    IntroIcon = "rbxassetid://123456",
    SaveConfig = true,
    ConfigFolder = "TestConfigs",
    ConfigFileName = "Settings.json",
    ShowLoadNotification = false,
})
```

### Tab

```lua
local ExampleTab = Window:MakeTab({
    Name = "Example Tab",
    Icon = "rbxassetid://4483345998",
})
```

### Notification

```lua
SwiftUI:MakeNotification({
    Name = "Example Name",
    Content = "Example Content",
    Time = 3
})
```

### Section

```lua
ExampleTab:AddSection({
    Name = "Example Section"
})
```

### Toggle

```lua
ExampleTab:AddToggle({
    Name = "Example Toggle",
    Default = false,
    Callback = function(Value)
        print("Test Toggle Value: " .. tostring(Value))
    end
})
```

### Slider

```lua
ExampleTab:AddSlider({
    Name = "Example Slider",
    Min = 0,
    Max = 100,
    Default = 50,
    Increment = 1,
    Callback = function(Value)
        print("Test Slider Value: " .. tostring(Value))
    end
})
```

### Button

```lua
ExampleTab:AddButton({
    Name = "Example Button",
    Callback = function()
        print("Test Button Clicked")
    end
})
```

### Keybind

```lua
ExampleTab:AddBind({
    Name = "Example Keybind",
    Default = Enum.KeyCode.LeftControl,
    Callback = function()
        print("Test Keybind Pressed")
    end
})
```

### Texbox

```lua
ExampleTab:AddTextbox({
    Name = "Example Textbox",
    Default = "",
    TextDisappear = true,
    Callback = function(Value)
        print("Test Textbox Value: " .. Value)
    end
})
```

### Dropdown

```lua
ExampleTab:AddDropdown({
    Name = "Example Dropdown",
    Options = {"Option 1", "Option 2", "Option 3"},
    Default = "Option 1",
    Callback = function(Value)
        print("Test Dropdown Value: " .. Value)
    end
})
```

### Colorpick

```lua
ExampleTab:AddColorpicker({
    Name = "Example Colorpicker",
    Default = Color3.fromRGB(255, 0, 0),
    Callback = function(Value)
        highlightColor = Value
        print("Ausgewählte Farbe:", Value)
    end
})
```

### Paragraph

```lua
ExampleTab:AddParagraph("Example Paragraph", "This is an example paragraph. You can add more text here to provide information or instructions.")
```

### Labels

```lua
ExampleTab:AddLabel("Example Label")
```

### You want to use Swift for your Project?
Than join our discord with the link below
https://discord.gg/swift-library
