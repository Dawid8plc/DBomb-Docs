# [Players](../Players.md).Launch

## Declaration
[Players](../Players.md).<b>Launch</b>(number <b>PlayerID</b>, [Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Speed</b>)

## Description
Launches the specified player towards <b>Position</b> with <b>Speed</b>. Launching works similar to the [Launcher](../Tiles/Launcher.md) tile.

```lua
--Launches the second player towards the center of the map
local allPlayers = Players.GetAll();
local world = World.GetSettings();

Players.Launch(allPlayers[2], V3(world.Width / 2, 1, world.Height / 2), 1);
```

---

## Declaration
[Players](../Players.md).<b>Launch</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>, [Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Speed</b>)

## Description
Launches the specified player(s) towards <b>Position</b> depending on the <b>Mode</b> with <b>Speed</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed. Launching works similar to the [Launcher](../Tiles/Launcher.md) tile.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.
```lua
--Launches other team members of the specified player
local allPlayers = Players.GetAll();
Players.Launch(allPlayers[1], TargetPlayer.OtherTeamMembers, Vector3.zero, V3(2, 1, 5), 1);

--Launches the furthest player from the provided point, PlayerID doesn't matter
local point = V3(2, 1, 3);
Players.Launch(0, TargetPlayer.Furthest, point, V3(2, 1, 5), 1);
```

---

## Declaration
[Players](../Players.md).<b>Launch</b>(Dictionary\<number> <b>PlayerIDs</b>, [Vector3](../Types/Vector3.md) <b>Position</b>, number <b>Speed</b>)

## Description
Launches the specified players towards <b>Position</b> with <b>Speed</b>. Launching works similar to the [Launcher](../Tiles/Launcher.md) tile.

```lua
--Launches everyone towards a certain position
local allPlayers = Players.GetAll();
Players.Launch(allPlayers, V3(2, 1, 5), 1);

--Launches only the players that have enough bombs
local toTeleport = {};
for i, player in ipairs(allPlayers) do 
    if player.BombsTotal > 5 then
        table.insert(toTeleport, player);
    end
end

Players.Launch(toTeleport, V3(2, 1, 5), 1);

--Launches only the first two players
Players.Launch({allPlayers[1], allPlayers[2]}, V3(2, 1, 5), 1);
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.