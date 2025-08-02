# [Game](../Game.md).SpawnBomb

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Power</b>, bool <b>PlaySound</b>)

## Description
Spawns a Bomb at a given <b>Position</b> with provided <b>Power</b>. <b>PlaySound</b> decides if the ticking sound effect should be played.

```lua
local SpawnPos = V3(5, 2, 3);
local BlastRadius = 5;

Game.SpawnBomb(SpawnPos, BlastRadius);
```

---

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Power</b>, bool <b>PlaySound</b>, [Direction](../Types/Direction.md) <b>PushDirection</b>)

## Description
Spawns a Bomb at a given <b>Position</b> with provided <b>Power</b>, and then pushes it in the <b>PushDirection</b> direction. <b>PlaySound</b> decides if the ticking sound effect should be played.

```lua
local Push = Direction.Right;

Game.SpawnBomb(V3(2, 1, 2), 3, Push);
```

---

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Power</b>, bool <b>PlaySound</b>, [Vector3](../Types/Vector3.md)  <b>LaunchTarget</b>, number <b>Speed</b>)

## Description
Spawns a Bomb at a given <b>Position</b> with provided <b>Power</b>, and then launches it towards <b>LaunchTarget</b> position with <b>Speed</b>. Launching works similar to the [Launcher](../Tiles/Launcher.md) tile. <b>PlaySound</b> decides if the ticking sound effect should be played.

```lua
local Position = V3(1, 0, 5);
local Power = 2;
local LaunchTarget = V3(10, 1, 10);
local Speed = 1;
Game.SpawnBomb(Position, Power, LaunchTarget, Speed);
```

---

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, number <b>Power</b>, bool <b>PlaySound</b>)

## Description
Spawns a Bomb at a given Tile located at <b>Position</b> on <b>Layer</b> with provided <b>Power</b>. <b>PlaySound</b> decides if the ticking sound effect should be played.
<br> 
<br>Bomb placement is more accurate when using this method on Slopes.
<br>
<br>Works similar to the Spawn Bomb trigger action.

```lua
local SpawnPos = V2(2, 1);
local Layer = 0;
local BlastRadius = 2;

Game.SpawnBomb(SpawnPos, Layer, BlastRadius);
```

---

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, number <b>Power</b>, bool <b>PlaySound</b>, [Direction](../Types/Direction.md) <b>PushDirection</b>)

## Description
Spawns a Bomb at a given Tile located at <b>Position</b> on <b>Layer</b> with provided <b>Power</b>, and then pushes it in the <b>PushDirection</b> direction. <b>PlaySound</b> decides if the ticking sound effect should be played.
<br> 
<br>Bomb placement is more accurate when using this method on Slopes.
<br>
<br>Works similar to the Spawn Bomb trigger action.

```lua
local PushDir = Direction.Up;

Game.SpawnBomb(V2(3, 5), 0, 2, PushDir);
```

---

## Declaration
[Game](../Game.md).<b>SpawnBomb</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, number <b>Power</b>, bool <b>PlaySound</b>, [Vector3](../Types/Vector3.md)  <b>LaunchTarget</b>, number <b>Speed</b>)

## Description
Spawns a Bomb at a given Tile located at <b>Position</b> on <b>Layer</b> with provided <b>Power</b>, and then launches it towards <b>LaunchTarget</b> position with <b>Speed</b>. Launching works similar to the [Launcher](../Tiles/Launcher.md) tile. <b>PlaySound</b> decides if the ticking sound effect should be played.
<br> 
<br>Bomb placement is more accurate when using this method on Slopes.
<br>
<br>Works similar to the Spawn Bomb trigger action.

```lua
local Position = V2(1, 5);
local Layer = 0;
local Power = 2;
local LaunchTarget = V3(10, 1, 10);
local Speed = 1;
Game.SpawnBomb(Position, Layer, Power, LaunchTarget, Speed);
```