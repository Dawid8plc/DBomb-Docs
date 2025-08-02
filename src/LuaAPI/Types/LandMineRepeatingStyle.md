# LandMineRepeatingStyle

Enumeration that represents the different repeating styles for the LandMine tile.

## Values
| | |
| -------- | ------- |
| <b>None</b> [0]  | LandMine expires after being triggered once |
| <b>Step</b> [1]  | LandMine can be triggered several times by stepping on it |
| <b>Repeat</b> [2]  | LandMine explodes several times in a row with a delay |

## Examples
```lua
local noRepeat = LandMineRepeatingStyle.None;

local stepRepeat = LandMineRepeatingStyle.Step;

local repeatRepeat = LandMineRepeatingStyle.Repeat;
```