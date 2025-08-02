# [World](../World.md).SetTile

## Declaration
[World](../World.md).<b>SetTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, [TileType](../Types/TileType.md) <b>Type</b>, Dictionary <b>Properties</b>)

## Description
Sets the tile at <b>Position</b> on <b>Layer</b> to <b>Type</b> and then modifies the provided <b>Properties</b>.

```lua
local layer = 0;

--Sets a specific tile to Wall
local wallPos = V2(7, 3);
World.SetTile(wallPos, layer, TileType.Wall, {});

--Sets a specific tile to PowerupTile, with changed properties
local powerupPos = V2(8, 3);
World.SetTile(powerupPos, layer, TileType.PowerupTile, {Bombs = 1, BlastRadius = 5});

--Sets a specific tile to Laser, with changed properties

--Define the color gradient for the laser
local colorGradient = ColorGradient();
colorGradient.AddColor(Color(252, 186, 3, 255), 0);
colorGradient.AddColor(Color(45, 252, 3, 255), 0.5);
colorGradient.AddColor(Color(98, 3, 252, 255), 1);
colorGradient.AddAlpha(255, 0);
colorGradient.AddAlpha(255, 1);

local laserPos = V2(9, 3);
World.SetTile(laserPos, layer, TileType.Laser, {LaserGradient = colorGradient, Range = 3, Enabled = false});
```

---

## Declaration
[World](../World.md).<b>SetTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, [TileType](../Types/TileType.md) <b>Type</b>, Dictionary <b>Properties</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) Origin)

## Description
Sets the tile at <b>Position</b> on <b>Layer</b> to <b>Type</b> and then modifies the provided <b>Properties</b>. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
local layer = 0;
local currentTile = GetCurrentTile();

--Sets the tile under the ScriptTile to a LandMine
local relativePos = V2(0, -1);
World.SetTile(relativePos, layer, TileType.LandMine, {Delay = 5}, true, currentTile.Position);
```

---

## Declaration
[World](../World.md).<b>SetTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, [TileType](../Types/TileType.md) <b>Type</b>, Dictionary <b>Properties</b>)

## Description
Sets the tiles at <b>Positions</b> on <b>Layer</b> to <b>Type</b> and then modifies the provided <b>Properties</b>.

```lua
local layer = 0;

--Sets several tiles to MetalCrate
local positions = {V2(4, 4), V2(5, 4), V2(6, 4)};
World.SetTile(positions, layer, TileType.MetalCrate, {});
```

---

## Declaration
[World](../World.md).<b>SetTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, [TileType](../Types/TileType.md) <b>Type</b>, Dictionary <b>Properties</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Sets the tiles at <b>Positions</b> on <b>Layer</b> to <b>Type</b> and then modifies the provided <b>Properties</b>. <b>Positions</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
local layer = 0;
local currentTile = GetCurrentTile();

--Sets several tiles diagonally relative to the ScriptTile
local relativePositions = {V2(2, 2), V2(2, -2), V2(-2, -2), V2(-2, 2)};
World.SetTile(relativePositions, layer, TileType.CountBomb, {BlastRadius = 10}, true, currentTile.Position);
```

---

## Note
Not all properties of a particular tile have to be passed into this method, only the ones you want to set.

To see which properties can be modified, check out the Tiles category, or alternatively, use the Edit mode in the Level Editor to see what properties specific tiles have in the Tile Settings panel.