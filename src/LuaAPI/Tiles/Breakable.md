# Breakable

## Properties
| | |
| -------- | ------- |
| number <b>MaxHealth</b> | The max health of this Breakable tile |
| number <b>Health</b> | The starting health of this Breakable tile |
| number <b>CurrentHealth</b> | The current health of this Breakable tile |
| number <b>ExplosionDamage</b> | How much damage an explosion does to this Breakable tile |
| number <b>LaserDamage</b> | How much damage a laser does to this Breakable tile |
| bool <b>SpawnRandomPowerup</b> | Whether this Breakable tile has the chance to spawn a Powerup, just like [Crates](../Tiles/Crate.md) do |
| [Color](../Types/Color.md) <b>Color</b> | The color of this Breakable tile |
| bool <b>DontApplyHealth</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from resetting its <b>Health</b> value upon using [ModTile](../WorldAPI/ModTile.md) |