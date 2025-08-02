# PowerupContainer

Object that is a container for powerups. Used with the [SetPowerups](../PlayersAPI/SetPowerups.md) function.

## Constructors
<b>Powerups</b>()


## Properties
| | |
| -------- | ------- |
| number <b>BlastRadius</b>  | How much Blast Radius should be given |
| number <b>Bombs</b> | How many Bombs should be given |
| number <b>Speed</b> | How much Speed should be given |
| bool <b>GrantsShield</b> | Whether Shield should be granted |
| bool <b>GrantsPushing</b> | Whether Pushing should be granted |
| bool <b>GrantsJumping</b> | Whether Jumping should be granted |

## Examples
```lua
local container = Powerups();
container.BlastRadius = 2;
container.Bombs = 5;
container.Speed = 1;
container.GrantsShield = true;
container.GrantsPushing = true;
container.GrantsJumping = false;
```