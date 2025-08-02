# PusherRotationStyle

Enumeration that represents the different rotation styles for the Pusher tile.

## Values
| | |
| -------- | ------- |
| <b>None</b> [0]  | Pusher doesn't rotate |
| <b>Clockwise</b> [1]  | Pusher rotates clockwise |
| <b>CounterClockwise</b> [2]  | Pusher rotates counter clockwise |
| <b>Random</b> [3]  | Pusher rotates randomly |

## Examples
```lua
local noneRotation = PusherRotationStyle.None;

local clockwiseRotation = PusherRotationStyle.Clockwise;

local randomRotation = PusherRotationStyle.Random;
```