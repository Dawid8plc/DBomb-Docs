# [Players](../Players.md).Teleport

## Declaration
[Players](../Players.md).<b>Teleport</b>(number <b>PlayerID</b>, [Vector3](../Types/Vector3.md) <b>Position</b>)

## Description
Teleports the specified player to <b>Position</b>

```lua
--Teleports the second player to the center of the map
local allPlayers = Players.GetAll();
local world = World.GetSettings();

Players.Teleport(allPlayers[2], V3(world.Width / 2, 1, world.Height / 2));
```

---

## Declaration
[Players](../Players.md).<b>Teleport</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>, [Vector3](../Types/Vector3.md) <b>Position</b>)

## Description
Teleports the specified player(s) to <b>Position</b> depending on the <b>Mode</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.
```lua
--Teleports other team members of the specified player
local allPlayers = Players.GetAll();
Players.Teleport(allPlayers[1], TargetPlayer.OtherTeamMembers, Vector3.zero, V3(2, 1, 5));

--Teleports the furthest player from the provided point, PlayerID doesn't matter
local point = V3(2, 1, 3);
Players.Teleport(0, TargetPlayer.Furthest, point, V3(2, 1, 5));
```

---

## Declaration
[Players](../Players.md).<b>Teleport</b>(Dictionary\<number> <b>PlayerIDs</b>, [Vector3](../Types/Vector3.md) <b>Position</b>)

## Description
Teleports the specified players to <b>Position</b>.

```lua
--Teleports everyone to a certain position
local allPlayers = Players.GetAll();
Players.Teleport(allPlayers, V3(2, 1, 5));

--Teleports only the players that have enough bombs
local toTeleport = {};
for i, player in ipairs(allPlayers) do 
    if player.BombsTotal > 5 then
        table.insert(toTeleport, player);
    end
end

Players.Teleport(toTeleport, V3(2, 1, 5));

--Teleports only the first two players
Players.Teleport({allPlayers[1], allPlayers[2]}, V3(2, 1, 5));
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.