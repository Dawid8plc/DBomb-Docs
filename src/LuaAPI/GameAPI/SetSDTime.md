# [Game](../Game.md).SetSDTime

## Declaration
[Game](../Game.md).<b>SetSDTime</b>(number <b>Time</b>)

## Description
Sets how many <b>Time</b> seconds until Sudden Death starts, but only if the timer hasn't stopped already.

```lua
--Gets the current Sudden Death time in seconds, adds 10 seconds to it,
--then sets the new time
local SDTime = Game.GetSDTime();
SDTime = SDTime + 10;

Game.SetSDTime(SDTime);
```