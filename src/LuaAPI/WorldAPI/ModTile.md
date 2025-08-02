# [World](../World.md).ModTile

## Declaration
[World](../World.md).<b>ModTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, Dictionary <b>Properties</b>)

## Description
Modifies the provided <b>Properties</b> for a tile at <b>Position</b> on <b>Layer</b>.

```lua
local layer = 0;

--Rotates the stairs to face the right direction
local stairs = V2(3, 5);
local stairProperties = {Direction = Direction.Right};
World.ModTile(stairs, layer, stairProperties);

--Changes the color of a Launcher tile (spring) to cyan
local launcher = V2(5, 5);
local launcherProperties = {Color = Color(0, 255, 255, 255)};
World.ModTile(launcher, layer, launcherProperties);

--Changes the color of a Pusher tile to red, makes it reignite bombs and invert bomb movement on contact
local pusher = V2(5, 3);
local pusherProperties = {ReignitesBomb = true, InvertsBombMovement = true, Color = Color(255, 0, 0, 255)};
World.ModTile(pusher, layer, pusherProperties);

--Changes the color of a Pusher tile to red, makes it reignite bombs and invert bomb movement on contact
local powerup = V2(7, 3);
local powerupProperties = {BlastRadius = 2, GrantsShield = true, GrantsJumping = false};
World.ModTile(powerup, layer, powerupProperties);
```

---

## Declaration
[World](../World.md).<b>ModTile</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, Dictionary <b>Properties</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Modifies the provided <b>Properties</b> for a tile at <b>Position</b> on <b>Layer</b>. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
local layer = 0;
local currentTile = GetCurrentTile();

--Disables the spikes above the ScriptTile
local relativePos = V2(0, 1);
local spikeProps = {ONDuration = -1, OFFDuration = -1};
World.ModTile(relativePos, layer, spikeProps, true, currentTile.Position);
```

---

## Declaration
[World](../World.md).<b>ModTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, Dictionary <b>Properties</b>)

## Description
Modifies the provided <b>Properties</b> for tiles at <b>Positions</b> on <b>Layer</b>.

```lua
local layer = 1;

--Detonates several CrateBombs
local positions = {V2(7, 5), V2(4, 3)};
local props = {Detonate = true};

World.ModTile(positions, layer, props);
```

---

## Declaration
[World](../World.md).<b>ModTile</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, Dictionary <b>Properties</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>)

## Description
Modifies the provided <b>Properties</b> for tiles at <b>Positions</b> on <b>Layer</b>. <b>Positions</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
local layer = 1;
local currentTile = GetCurrentTile();

--Makes the three lasers near the ScriptTile spin, and changes their color
local relativePositions = {V2(0, 1), V2(1, 1), V2(2, 1)};

--Define the color gradient for the laser
local colorGradient = ColorGradient();
colorGradient.AddColor(Color(252, 186, 3, 255), 0);
colorGradient.AddColor(Color(45, 252, 3, 255), 0.5);
colorGradient.AddColor(Color(98, 3, 252, 255), 1);
colorGradient.AddAlpha(255, 0);
colorGradient.AddAlpha(255, 1);

local laserProps = {LaserGradient = colorGradient, ConstantRotation = V3(0, 2, 0)};
World.ModTile(relativePositions, layer, laserProps, true, currentTile.Position);
```

---

## Note
Not all properties of a particular tile have to be passed into this method, only the ones you want to set.

To see which properties can be modified, check out the Tiles category, or alternatively, use the Edit mode in the Level Editor to see what properties specific tiles have in the Tile Settings panel.