# [Players](../Players.md).SetPowerups

## Declaration
[Players](../Players.md).<b>SetPowerups</b>(number <b>PlayerID</b>, [PowerupContainer](../Types/PowerupContainer.md) <b>Powerups</b>, [Operation](../Types/Operation.md) <b>Operation</b>)

## Description
Adds, sets or subtracts powerups for a player, depending on <b>Operation</b>.

Powerups such as Bombs, Blast Radius and Speed are stored as numbers in the <b>Powerups</b> container, so if <b>Operation</b> equals <b>Add</b>, then the provided amount of them will be given to the player. And likewise, if <b>Operation</b> equals <b>Subtract</b>, then the given amount will be taken away from the player. Last but not least, <b>Operation.Set</b> will overwrite the powerups of a player entirely.

In case of powerups such as Shield, Pushing and Jumping, which are booleans, they will be given or taken away depending on whether or not they're set to <b>true</b>. That is, if <b>Operation</b> equals <b>Add</b>, and <b>GrantsShield</b> is set to <b>true</b>, then it will be given to the player. And if <b>Operation</b> is set to <b>Subtract</b>, while <b>GrantsShield</b> is set to <b>true</b>, it will be taken away.

```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Creates a PowerupContainer object, and fills it with values
local powers = Powerups();
powers.BlastRadius = 5;
powers.Bombs = 2;
powers.Speed = 3;
powers.GrantsShield = true;
powers.GrantsPushing = false;
powers.GrantsJumping = true;

--Gives the first player the powerups
Players.SetPowerups(allPlayers[1], powers, Operation.Add);

--Takes the powerups from the first player
Players.SetPowerups(allPlayers[1], powers, Operation.Subtract);

--Sets first player's powerups to the contents of the container
Players.SetPowerups(allPlayers[1], powers, Operation.Set);
```

---

## Declaration
[Players](../Players.md).<b>SetPowerups</b>(number <b>PlayerID</b>, [TargetPlayer](../Types/TargetPlayer.md) <b>Mode</b>, [Vector3](../Types/Vector3.md) <b>Origin</b>, [PowerupContainer](../Types/PowerupContainer.md) <b>Powerups</b>, [Operation](../Types/Operation.md) <b>Operation</b>)

## Description
Adds, sets or subtracts powerups for specific players, depending on <b>Operation</b> and <b>Mode</b>. If using <b>Mode</b> set to <b>Closest</b> or <b>Furthest</b>, the <b>Origin</b> parameter will be used as the point of reference, otherwise [Vector3](../Types/Vector3.md).zero can be passed.

Powerups such as Bombs, Blast Radius and Speed are stored as numbers in the <b>Powerups</b> container, so if <b>Operation</b> equals <b>Add</b>, then the provided amount of them will be given to the player. And likewise, if <b>Operation</b> equals <b>Subtract</b>, then the given amount will be taken away from the player. Last but not least, <b>Operation.Set</b> will overwrite the powerups of a player entirely.

In case of powerups such as Shield, Pushing and Jumping, which are booleans, they will be given or taken away depending on whether or not they're set to <b>true</b>. That is, if <b>Operation</b> equals <b>Add</b>, and <b>GrantsShield</b> is set to <b>true</b>, then it will be given to the player. And if <b>Operation</b> is set to <b>Subtract</b>, while <b>GrantsShield</b> is set to <b>true</b>, it will be taken away.
<br>
<br>Check [TargetPlayer](../Types/TargetPlayer.md) for all possible <b>Mode</b> values.

```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Creates a PowerupContainer object, and fills it with values
local powers = Powerups();
powers.BlastRadius = 5;
powers.Bombs = 2;
powers.Speed = 3;
powers.GrantsShield = true;
powers.GrantsPushing = false;
powers.GrantsJumping = true;

--Gives everyone but the first player the powerups
Players.SetPowerups(allPlayers[1], TargetPlayer.Others, Vector3.zero, powers, Operation.Add);

--Takes away the powerups from a random player
Players.SetPowerups(0, TargetPlayer.Random, Vector3.zero, powers, Operation.Subtract);

--Sets the second player's powerups
Players.SetPowerups(allPlayers[2], TargetPlayer.Initiator, Vector3.zero, powers, Operation.Set);
```

---

## Declaration
[Players](../Players.md).<b>SetPowerups</b>(Dictionary\<number> <b>PlayerIDs</b>, [PowerupContainer](../Types/PowerupContainer.md) <b>Powerups</b>, [Operation](../Types/Operation.md) <b>Operation</b>)

## Description
Adds, sets or subtracts powerups for specific players, depending on <b>Operation</b>.

Powerups such as Bombs, Blast Radius and Speed are stored as numbers in the <b>Powerups</b> container, so if <b>Operation</b> equals <b>Add</b>, then the provided amount of them will be given to the player. And likewise, if <b>Operation</b> equals <b>Subtract</b>, then the given amount will be taken away from the player. Last but not least, <b>Operation.Set</b> will overwrite the powerups of a player entirely.

In case of powerups such as Shield, Pushing and Jumping, which are booleans, they will be given or taken away depending on whether or not they're set to <b>true</b>. That is, if <b>Operation</b> equals <b>Add</b>, and <b>GrantsShield</b> is set to <b>true</b>, then it will be given to the player. And if <b>Operation</b> is set to <b>Subtract</b>, while <b>GrantsShield</b> is set to <b>true</b>, it will be taken away.

```lua
--Retrieves all players
local allPlayers = Players.GetAll();

--Creates a PowerupContainer object, and fills it with values
local powers = Powerups();
powers.BlastRadius = 5;
powers.Bombs = 2;
powers.Speed = 3;
powers.GrantsShield = true;
powers.GrantsPushing = false;
powers.GrantsJumping = true;

--Gives everyone the powerups
Players.SetPowerups(allPlayers, powers, Operation.Add);

--Takes away the powerups specifically from player 2 and 4
Players.SetPowerups({allPlayers[2], allPlayers[4]}, powers, Operation.Add);

--Sets the second player's powerups
Players.SetPowerups(allPlayers[2], powers, Operation.Set);
```

---

## Note
Player IDs must be whole numbers.

Keep in mind the Player IDs aren't necessarily ordered. Players can join and leave in the lobby, potentially several times, increasing their ID, which is why using [Players](../Players.md).[GetAll](GetAll.md) is advised if you want to target a player at a specific slot.

You can also pass [Player](../Types/Player.md) objects instead of numbers as IDs.