# [Game](../Game.md).GetGameScheme

## Declaration
[Game](../Game.md).<b>GetGameScheme</b>()

## Description
Returns the [GameScheme](../Types/GameScheme.md) object with the match settings.

```lua
--Gets the game scheme and prints some of its settings in the Scripts Console
local scheme = Game.GetGameScheme();

Print("Starting Bombs: " .. scheme.StartingBombs);
Print("Starting Blast Radius: " .. scheme.StartingPower);
Print("Preserve Shield: " .. tostring(scheme.PreserveShield));
Print("Drop Chance: " .. scheme.DropChance);
Print("Impact Bombs: " .. tostring(scheme.ImpactBombs));
Print("Game mode: " .. tostring(scheme.GameMode));
```