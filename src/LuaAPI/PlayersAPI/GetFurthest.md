# [Players](../Players.md).GetFurthest

## Declaration
[Players](../Players.md).<b>GetFurthest</b>([Vector3](../Types/Vector3.md) <b>Position</b>)

## Description
Returns the [Player](../Types/Player.md) object for the furthest player relative to <b>Position</b>. If not found, returns a [Player](../Types/Player.md) object with <b>ID</b> set to -1.

```lua
--Prints out the name of the furthest player to the position in the Scripts Console
local position = V3(2, 1, 2);
local furthestPlayer = Players.GetFurthest(position);

Print(furthestPlayer.Name);
```

---

## Declaration
[Players](../Players.md).<b>GetFurthest</b>([Tile](../Types/Tile.md) <b>Tile</b>)

## Description
Returns the [Player](../Types/Player.md) object for the furthest player relative to <b>Tile</b>. If not found, returns a [Player](../Types/Player.md) object with <b>ID</b> set to -1.

```lua
--Prints out the name of the furthest player to the tile in the Scripts Console
local tile = World.GetTile(V2(1, 5), 0);
local furthestPlayer = Players.GetFurthest(position);

Print(furthestPlayer.Name);
```


