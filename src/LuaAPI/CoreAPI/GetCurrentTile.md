# GetCurrentTile

## Declaration
<b>GetCurrentTile</b>()

## Description
Returns the [Tile](../Types/Tile.md) object for the ScriptTile that is running the current script.

```lua
--Prints the position of the ScriptTile this script is running on
local currentTile = GetCurrentTile();

Print("X: " .. currentTile.Position.x .. " Y: " .. currentTile.Position.y);
```