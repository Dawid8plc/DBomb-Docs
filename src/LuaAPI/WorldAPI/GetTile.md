# [World](../World.md).GetTile

## Declaration
[World](../World.md).<b>GetTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>)

## Description
Returns the [Tile](../Types/Tile.md) object for a tile at <b>Position</b>.

```lua
--Gets the tile and prints its TileType and position to the Scripts Console
local position = V2(1, 1);
local layer = 0;
local tile = World.GetTile(position, layer);
Print(tile.Type);
Print("X: " .. tile.Position.x .. " Y: " .. tile.Position.y);
```

---

## Declaration
[World](../World.md).<b>GetTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>)

## Description
Returns the [Tile](../Types/Tile.md) objects for tiles at <b>Positions</b>.

```lua
--Gets the tiles and prints their TileTypes and positions to the Scripts Console
local positions = {V2(1, 1), V2(1, 2), V2(2, 1), V2(2, 2)};
local layer = 0;
local tiles = World.GetTile(positions, layer);

for i, tile in ipairs(tiles) do 
    Print(tile.Type);
    Print("X: " .. tile.Position.x .. " Y: " .. tile.Position.y);
end
```

---

## Declaration
[World](../World.md).<b>GetTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Returns the [Tile](../Types/Tile.md) object for a tile at <b>Position</b>. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
--Gets the tile to the right of the ScriptTile then prints its TileType and position to the Scripts Console
local currentTile = GetCurrentTile();
local relativePosition = V2(1, 0);
local layer = 0;
local relative = true;
local tile = World.GetTile(relativePosition, layer, relative, currentTile.Position);
Print(tile.Type);
Print("X: " .. tile.Position.x .. " Y: " .. tile.Position.y);
```

---

## Declaration
[World](../World.md).<b>GetTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Returns the [Tile](../Types/Tile.md) objects for tiles at <b>Positions</b>. <b>Positions</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
--Gets the tiles around the ScriptTile and prints their TileTypes and positions to the Scripts Console
local currentScriptTile = GetCurrentTile();
local positions = {V2(0, 1), V2(1, 1), V2(1, 0), V2(-1, 0), V2(-1, -1), V2(0, -1), V2(1, -1), V2(-1, 1)}
local layer = 0;
local tiles = World.GetTile(positions, layer, true, currentScriptTile.Position);

for i, tile in ipairs(tiles) do 
    Print(tile.Type);
    Print("X: " .. tile.Position.x .. " Y: " .. tile.Position.y);
end
```