# [Scripts](../Scripts.md).SetVar

## Declaration
[Scripts](../Scripts.md).<b>SetVar</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>, string <b>Name</b>, object <b>Value</b>)

## Description
Sets the <b>Name</b> variable value to <b>Value</b> for a <b>ScriptTile</b>.

```lua
--Gets the Tile object of the other ScriptTile, 
--and sets the value of the editor-exposed "BlastForce" variable to 5
local otherScriptTile = World.GetTile(V2(4, 5), 0);
Scripts.SetVar(otherScriptTile, "BlastForce", 5);
```

---

## Declaration
[Scripts](../Scripts.md).<b>SetVar</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>, Dictionary <b>Variables</b>)

## Description
Sets the <b>Variables</b> for a <b>ScriptTile</b>.

```lua
--Gets the Tile object of the other ScriptTile, 
--and sets the value of the editor-exposed "BlastForce" and "BlastPosition" variables
local otherScriptTile = World.GetTile(V2(4, 5), 0);
Scripts.SetVar(otherScriptTile, {BlastForce = 5, BlastPosition = V3(5, 1, 4)});
```

---

## Declaration
[Scripts](../Scripts.md).<b>SetVar</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>, string <b>Name</b>, object <b>Value</b>)

## Description
Sets the <b>Name</b> variable value to <b>Value</b> for <b>ScriptTiles</b>.

```lua
--Gets the Tile objects of the other ScriptTiles,
--and sets the value of the editor-exposed "BlastForce" variables to 5
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
Scripts.SetVar(otherScriptTiles, "BlastForce", 5);
```

---

## Declaration
[Scripts](../Scripts.md).<b>SetVar</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>, Dictionary <b>Variables</b>)

## Description
Sets the <b>Variables</b> for <b>ScriptTiles</b>.

```lua
--Gets the Tile objects of the other ScriptTiles, 
--and sets the value of the editor-exposed "BlastForce" and "BlastPosition" variables
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
Scripts.SetVar(otherScriptTiles, {BlastForce = 5, BlastPosition = V3(5, 1, 4)});
```