# TimerTrigger

Enumeration that represents the different events that can trigger a Timer tile.

## Values
| | |
| -------- | ------- |
| <b>None</b> [0]  | Timer isn't fired automatically |
| <b>OnStart</b> [1]  | Timer is fired when the round starts |
| <b>OnSuddenDeath</b> [2]  | Timer is fired when Sudden Death begins |
| <b>OnRoundEnd</b> [3]  | Timer is fired when the round ends|

## Examples
```lua
local noneTrigger = TimerTrigger.None;

local onStartTrigger = TimerTrigger.OnStart;

local suddenDeathTrigger = TimerTrigger.OnSuddenDeath;
```