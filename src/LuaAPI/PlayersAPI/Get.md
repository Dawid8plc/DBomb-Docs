# [Players](../Players.md).Get

## Declaration
[Players](../Players.md).<b>Get</b>(number <b>PlayerID</b>)

## Description
Retrieves the [Player](../Types/Player.md) object for the specified PlayerID, containing their name, powerups and other stats, otherwise returns a [Player](../Types/Player.md) object with <b>ID</b> set to -1 if the player doesn't exist.

```lua
--Prints the name of the player with ID 0 in the Scripts Console
local firstPlayer = Players.Get(0);
Print(firstPlayer.Name);
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.
