# [Players](../Players.md).GetAll

## Declaration
[Players](../Players.md).<b>GetAll</b>()

## Description
Retrieves the [Player](../Types/Player.md) objects for all the players, containing their name, powerups and other stats.

```lua
--Prints the names of all the players in the Scripts Console
local allPlayers = Players.GetAll();

for i, player in ipairs(allPlayers) do 
    Print(player.Name);
end
```