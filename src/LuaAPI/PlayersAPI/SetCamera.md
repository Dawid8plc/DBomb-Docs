# [Players](../Players.md).SetCamera

## Declaration
[Players](../Players.md).<b>SetCamera</b>(number <b>PlayerID</b>, [Vector3](../Types/Vector3.md) <b>PositionOffset</b>, [Vector3](../Types/Vector3.md) <b>RotationOffset</b>)

## Description
Sets position and rotation camera offsets respectively to <b>PositionOffset</b> and <b>RotationOffset</b> for a specific player.

```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Sets the first player's camera
Players.SetCamera(allPlayers[1], V3(0, 6, 7.6), V3(25, 0, 0));
```

---

## Declaration
[Players](../Players.md).<b>SetCamera</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>, [Vector3](../Types/Vector3.md) <b>PositionOffset</b>, [Vector3](../Types/Vector3.md) <b>RotationOffset</b>)

## Description
Sets position and rotation camera offsets respectively to <b>PositionOffset</b> and <b>RotationOffset</b> for specific players, depending on the <b>Mode</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.
```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Sets the camera for all the other teams than player 1's team
Players.SetCamera(allPlayers[1], TargetPlayer.OtherTeams, Vector3.zero, V3(0, 6, 7.6), V3(25, 0, 0));

--Sets the camera for everyone else than player 2
Players.SetCamera(allPlayers[2], TargetPlayer.Others, Vector3.zero, V3(0, 6, 7.6), V3(25, 0, 0));

--Sets the camera for the furthest player to the provided position
Players.SetCamera(0, TargetPlayer.Furthest, V3(2, 1, 2), V3(0, 6, 7.6), V3(25, 0, 0));
```

---

## Declaration
[Players](../Players.md).<b>SetCamera</b>(Dictionary\<number> <b>PlayerIDs</b>, [Vector3](../Types/Vector3.md) <b>PositionOffset</b>, [Vector3](../Types/Vector3.md) <b>RotationOffset</b>)

## Description
Sets position and rotation camera offsets respectively to <b>PositionOffset</b> and <b>RotationOffset</b> for specific players.

```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Sets the camera for everyone
Players.SetCamera(allPlayers, V3(0, 6, 7.6), V3(25, 0, 0));

--Sets different camera offsets for player 1 and 3 specifically
Players.SetCamera({allPlayers[1], allPlayers[3]}, V3(0.5, 0, 14), V3(0, 180, 0));
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.

If there are several players playing on the same device, and the camera gets set for one of them, it will set the camera for every player on that device.

This does not affect the FPS gamemode camera.