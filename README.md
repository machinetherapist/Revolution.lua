![GitHub Logo](https://composer-devil.com/images/revolutionbase.png)

# What is Revolution.lua
Revolution.lua is a menu base prepared with another perspective.
It has been developed in the most convenient way to Lua language, as a noob friendly.
It is very easy to create new menus because it uses array-based indexable design architecture instead of nested scripting.
Revolution.lua is not a standalone menu. In my spare time, I designed it in a way that I can easily add a troll option. Usage and menu making is simple and easy. Fully open to development!


# Benefits
You won't have to deal with nested queries in a scripting language like lua. And make sure this will make your job easier than you guessed.
Cleaner and readable coding as the layout is designed independently

# Drawbacks

Automatically indexes the order of the submenus. It is bad for user memorization.
Checkboxes and comboboxes are not available in the main menu


# Add Sub Menu 
```lua
-----------------------------------------------------------
-- Sub Menu
RevolutionBase.Initiator.Sub_Menu                   = {
	type = "Menu"
}
```
# Add Sub Sub Menu 
```lua
-----------------------------------------------------------
-- Sub Menu
RevolutionBase.Initiator.Sub_Menu.Sub_Menu           = {
	type = "Menu"
}
```
# Add Button
```lua
-----------------------------------------------------------
-- Sub Menu
RevolutionBase.Initiator.Sub_Menu.Sub_Menu.Button     = {
	type = "Button",
	action = function() print "ok" end
}
```
# Add Checkbox
```lua
-----------------------------------------------------------
-- Sub Menu
RevolutionBase.Initiator.Sub_Menu.Sub_Menu.Checkbox   = {
	type = "Checkbox",
	action = function(toggle)
		print(toggle)
	end
}
```
# Add Combobox
```lua
-----------------------------------------------------------
-- Sub Menu
RevolutionBase.Initiator.Sub_Menu.Sub_Menu.Combo     = {
	type = "Combobox",
	items = {'Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5'},
	currentItemIndex = 3,
	selectedItemIndex = 3,
	action = function(currentIndex, selectedItemIndex)
		print(currentIndex, selectedItemIndex)
	end
}
```
