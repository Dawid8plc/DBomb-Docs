# [Game](../Game.md).AwardWin

## Declaration
[Game](../Game.md).<b>AwardWin</b>(number <b>PlayerID</b>, number <b>Wins</b>, bool <b>LockWin</b>)

## Description
Awards <b>Wins</b> amount of wins to the player with the specified <b>PlayerID</b>. <b>LockWin</b> decides if the <b>Wins</b> can be lost by dying in the standard gamemode.
<br><br> Wins are only distributed once round ends, not instantly.

```lua
--Awards the first player with a win
local allPlayers = Players.GetAll();
Game.AwardWin(allPlayers[1], 1, false);
```

---

## Declaration
[Game](../Game.md).<b>AwardWin</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>, number <b>Wins</b>, bool <b>LockWin</b>)

## Description
Awards <b>Wins</b> amount of wins to the specified player(s), depending on the <b>Mode</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed. <b>LockWin</b> decides if the <b>Wins</b> can be lost by dying in the standard gamemode.
Wins are only distributed once round ends, not instantly.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.

```lua
--Awards everyone but the player with ID 2 with a win
local DontAward = 2;
local Mode = TargetPlayer.Others;
Game.AwardWin(DontAward, Mode, Vector3.zero, 1, false);

--Awards the third player with a win
local allPlayers = Players.GetAll();
Game.AwardWin(allPlayers[3], 1, false);

--Awards everyone on the same team as the passed player with a win
Game.AwardWin(1, TargetPlayer.AllTeamMembers, Vector3.zero, 1, false);

--Awards a random player with a win, the PlayerID parameter is not used
Game.AwardWin(0, TargetPlayer.Random, Vector3.zero, 1, false);

--Awards the closest player to the middle of the map with a win, PlayerID is once more not used
local world = World.GetSettings();
Game.AwardWin(0, TargetPlayer.Closest, V3(world.Width / 2, 1, world.Height / 2), 1, false);
```

---

## Declaration
[Game](../Game.md).<b>AwardWin</b>(Dictionary\<number> <b>PlayerIDs</b>, number <b>Wins</b>, bool <b>LockWin</b>)

## Description
Awards <b>Wins</b> amount of wins to the specified players. <b>LockWin</b> decides if the <b>Wins</b> can be lost by dying in the standard gamemode.
<br><br> Wins are only distributed once round ends, not instantly.

```lua
--Retrieves every single player and awards them wins
local allPlayers = Players.GetAll();
Game.AwardWin(allPlayers, 1, false);

--Awards the second and fourth players with two wins and locks them
Game.AwardWin({allPlayers[2], allPlayers[4]}, 2, true);
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](../PlayersAPI/GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.
