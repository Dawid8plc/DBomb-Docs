# [Game](../Game.md).SpawnExplosion

## Declaration
[Game](../Game.md).<b>SpawnExplosion</b>([Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Power</b>)

## Description
Spawns an Explosion at a given <b>Position</b> with provided <b>Power</b>.

```lua
local SpawnPos = V3(5, 0.5, 3);
local BlastRadius = 5;

Game.SpawnExplosion(SpawnPos, BlastRadius);
```

---

## Declaration
[Game](../Game.md).<b>SpawnExplosion</b>([Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Power</b>, bool <b>DontOptimize</b>, bool <b>DontOptimizeTrigger</b>, bool <b>PreventNormalExplosionOptimization</b>)

## Description
Spawns an Explosion at a given <b>Position</b> with provided <b>Power</b>.

<b>DontOptimize</b> if set to <b>true</b> will cause this explosion to overlap other normal explosions.

<b>DontOptimizeTrigger</b> if set to <b>true</b> will cause this explosion to overlap other trigger or script spawned explosions.

<b>PreventNormalExplosionOptimization</b> if set to <b>true</b> will cause other explosions to overlap this one.

All of these options should be used sparingly. When an explosion is about to spawn at a position, the game looks for an existing one there, and if it finds one, it resets the timer on that explosion instead of spawning another one, for performance reasons. These options effectively prevent that from happening, and if used frequently could lead to worse performance.

```lua
local SpawnPos = V3(5, 0.5, 3);
local BlastRadius = 5;

Game.SpawnExplosion(SpawnPos, BlastRadius, true, true, true);
```