# [World](../World.md).SetTileHeight

## Declaration
[World](../World.md).<b>SetTileHeight</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, number <b>Height</b>, number <b>ExtendCount</b>)

## Description
Sets the desired <b>Height</b> and <b>ExtendCount</b> on a specific tile at <b>Position</b> on <b>Layer</b>.

```lua
--Sets the tile height at position "target" and "layer" 0 to 3 and extend count to 1
local target = V2(1, 2);
local layer = 0;
local height = 3;
local extendCount = 1;

World.SetTileHeight(target, layer, height, extendCount);
```

---

## Declaration
[World](../World.md).<b>SetTileHeight</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, number <b>Height</b>, number <b>ExtendCount</b>)

## Description
Sets the desired <b>Height</b> and <b>ExtendCount</b> on specific tiles at <b>Positions</b> on <b>Layer</b>.

```lua
--Sets the tile height at provided positions to 3 and extend count to 1
local targets = {V2(1, 2), V2(1, 3), V2(1, 4), V2(1, 5), V2(2,2), V2(2,3), V2(2,4), V2(2,5)};
local layer = 0;
local height = 3;
local extendCount = 1;

World.SetTileHeight(targets, layer, height, extendCount);
```

---

## Declaration
[World](../World.md).<b>SetTileHeight</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, number <b>Height</b>, number <b>ExtendCount</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Sets the desired <b>Height</b> and <b>ExtendCount</b> on a specific tile at <b>Position</b> on <b>Layer</b>. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
--Sets the tile height on the tile above the ScriptTile to 3 and extend count to 1
local currentScriptTile = GetCurrentTile();
local layer = 0;
local height = 3;
local extendCount = 1;

World.SetTileHeight(V2(0, 1), layer, height, extendCount, true, currentScriptTile.Position);
```

---

## Declaration
[World](../World.md).<b>SetTileHeight</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, number <b>Height</b>, number <b>ExtendCount</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Sets the desired <b>Height</b> and <b>ExtendCount</b> on specific tiles at <b>Positions</b> on <b>Layer</b>. <b>Positions</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
--Sets the tile height on all the tiles around the ScriptTile to 3 and extend count to 1
local currentScriptTile = GetCurrentTile();
local targets = {V2(0, 1), V2(1, 1), V2(1, 0), V2(-1, 0), V2(-1, -1), V2(0, -1), V2(1, -1), V2(-1, 1)}
local layer = 0;
local height = 3;
local extendCount = 1;

World.SetTileHeight(targets, layer, height, extendCount, true, currentScriptTile.Position);
```