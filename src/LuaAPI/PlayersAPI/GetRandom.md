# [Players](../Players.md).GetRandom

## Declaration
[Players](../Players.md).<b>GetRandom</b>()

## Description
Returns the [Player](../Types/Player.md) object for a random alive player, otherwise returns a [Player](../Types/Player.md) object with <b>ID</b> set to -1.

```lua
--Prints out the name of a random player in the Scripts Console
local randomPlayer = Players.GetRandom();

Print(randomPlayer.Name);
```

