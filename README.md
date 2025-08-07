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
ContextActionService:SetPosition("Sprint", UDim2.new(.7, 0, -0.2, 0))
ContextActionService:SetTitle("Sprint", "Sprint")

-- Apply default style to the button
CAO.default(ContextActionService:GetButton("Sprint"))
```
### with module use default
<img width="1287" height="593" alt="RobloxScreenShot20250807_021937082" src="https://github.com/user-attachments/assets/f4ad76c6-0881-40bb-86de-ee14f2e2219b" />

### without module
<img width="1287" height="593" alt="RobloxScreenShot20250807_022037352" src="https://github.com/user-attachments/assets/331584eb-2f7c-4a60-b808-9f1e7474489c" />

## 📄 API Reference

## Functions

### **.default(button)**
```lua
CAO.default(ContextActionService:GetButton("Button"))
```
Apply the default button style

### .custom(...)
```lua
CAO.custom(ContextActionService:GetButton("Button"), 
	ContextImage:AssetID,
	ContextTransparency: number,
	ContextColor3: Color3,
	ActionTransparency: number,
	ActionColor3: Color3, 
	TextFont: Font)
```
Fully customizable context button styling 


### .legacy(button)
```lua
CAO.default(ContextActionService:GetButton("Button"))
```
Apply legacy default use two image button design

### .custom_legacy(...)
```lua
CAO.custom_legacy((ContextActionService:GetButton("Button"), 
	ContextImageDefault:AssetID, 
	ContextImagePressed:AssetID,
	ContextTransparency: number,
	ContextColor3: Color3,
	ActionTransparency: number,
	ActionColor3: Color3, 
	TextFont: Font)
```
Mix of legacy behavior with full customization

## Methods

### :SetButtonSize(number)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetButtonSize(number)
```
Set button size in pixel 

### :SetContextColor(Color3)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetContextColor(Color3)
```
Set the background (context) color of the button

### :SetContextTransparency(number)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetContextTransparency(number)
```
Set transparency of the button

### :SetFont(font)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetFont(font)
```
Set the font for the button's text

### :SetTextSize(number)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetTextSize(number)
```
Set the text size in pixel for the button's text

### :SetActionColor(Color3)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetActionColor(color)
```
Set the color of the button's text and icon

### :SetActionTransparency(number)
```lua
local default = CAO.default(ContextActionService:GetButton("Button"))
default:SetActionTransparency(number)
```
Set transparency for icon and text label


## 💬 Credits
Created by **MBAID**
Inspired to create this module by **M100 (Micamaster100)** — whose work and ideas sparked the original motivation.
Also influenced by **TopBarPlus** for its clean API and modular structure.
