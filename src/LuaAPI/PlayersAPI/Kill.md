# [Players](../Players.md).Kill

## Declaration
[Players](../Players.md).<b>Kill</b>(number <b>PlayerID</b>)

## Description
Kills the player with the specified <b>PlayerID</b>.

```lua
--Kills the first player
local allPlayers = Players.GetAll();
Players.Kill(allPlayers[1]);
```

---

## Declaration
[Players](../Players.md).<b>Kill</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>)

## Description
Kills the specified player(s), depending on the <b>Mode</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.
```lua
--Kills everyone but the player with ID 2
local DontKill = 2;
local Mode = TargetPlayer.Others;
Players.Kill(DontKill, Mode, Vector3.zero);

--Kills the third player
local allPlayers = Players.GetAll();
Players.Kill(allPlayers[3]);

--Kills everyone on the same team as the passed player
Players.Kill(1, TargetPlayer.AllTeamMembers, Vector3.zero);

--Kills random player, the PlayerID parameter is not used
Players.Kill(0, TargetPlayer.Random, Vector3.zero);

--Kills the closest player to the middle of the map, PlayerID is once more not used
local world = World.GetSettings();
Players.Kill(0, TargetPlayer.Closest, V3(world.Width / 2, 1, world.Height / 2));
```

---

## Declaration
[Players](../Players.md).<b>Kill</b>(Dictionary\<number> <b>PlayerIDs</b>)

## Description
Kills the specified players.

```lua
--Retrieves every single player and kills them
local allPlayers = Players.GetAll();
Players.Kill(allPlayers);

--Kills the second and fourth players
Players.Kill({allPlayers[2], allPlayers[4]});
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.
