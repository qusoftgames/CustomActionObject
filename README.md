# CustomActionObject (CAO)

<img width="349" height="125" alt="logo_22_macro" src="https://github.com/user-attachments/assets/6ca7a63a-7bd7-4cac-9caf-3f2a9f4d9ee1" />

A simple way to create customized mobile button designs for Roblox ContextActionService

**CustomActionObject (CAO)** is a lightweight module designed to give developers full control over the visual style of mobile buttons created by `ContextActionService`.  
Since Roblox hasn't updated the look of mobile buttons in a long time, I created this module to make it easier to customize and restyle them the way you want.

## Why Use CAO?
Unlike most solutions, **CAO** doesn’t require you to create your own GUI for mobile buttons.
Everything is based on Roblox’s built-in `ContextActionService`.

You don’t need to add extra buttons or panels to your game.
**CAO** simply restyles the default ContextActionService buttons, giving them a clean and customizable look.

## 📦 Installation

Just drop the module into `ReplicatedStorage` (or any module folder you use).  
Then require it from a LocalScript:

```lua
local CAO = require(game.ReplicatedStorage.CustomActionObject)
```
## 🔧 Basic Usage
```lua
local ContextActionService = game:GetService("ContextActionService")
local CAO = require(game.ReplicatedStorage.CustomActionObject)

-- Bind your mobile action
ContextActionService:BindAction("Sprint", function() end, true)
ContextActionService:SetPosition("Sprint", UDim2.new(0.1, 0, 0.5, 0))
ContextActionService:SetTitle("Sprint", "Sprint")

-- Apply default style to the button
CAO.default(ContextActionService:GetButton("Sprint"))
```

## 📄 API Reference (WIP)

| Method                           | Description                               |
| -------------------------------- | ----------------------------------------- |
| `.default(button)`               | Apply the default button style            |
| `.legacy(button)`                | Apply an older-style button design        |
| `.custom(...)`                   | Fully customizable context button styling |
| `.custom_legacy(...)`            | Mix of legacy behavior and full styling   |
| `.SetFont(font)`                 | Set font for button text                  |
| `.SetActionColor(color)`         | Set color for text & icon                 |
| `.SetContextColor(color)`        | Set color for background image            |
| `.SetActionTransparency(value)`  | Set transparency of icon & label          |
| `.SetContextTransparency(value)` | Set background image transparency         |


## 💬 Credits
Created by **MBAID**
Inspired to create this module by **M100 (Micamaster100)** — whose work and ideas sparked the original motivation.
Also influenced by **TopBarPlus** for its clean API and modular structure.
