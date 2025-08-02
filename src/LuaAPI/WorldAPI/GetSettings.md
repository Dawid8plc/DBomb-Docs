# [World](../World.md).GetSettings

## Declaration
[World](../World.md).<b>GetSettings</b>()

## Description
Returns the world settings in the form of a [World](../Types/World.md) object.

```lua
--Gets the World object and prints its properties to the Scripts Console
local world = World.GetSettings();
Print("World Name: " .. world.Name);
Print("Author: " .. world.Author);
Print("Width: " .. world.Width);
Print("Height: " .. world.Height);
```