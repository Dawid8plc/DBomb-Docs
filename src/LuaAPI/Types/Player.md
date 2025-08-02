# Player

Object that represents a player in the game.

## Properties
| | |
| -------- | ------- |
| number <b>ID</b>  | ID of the player |
| string <b>Name</b> | Name of the player |
| bool <b>Killed</b>  | Whether the player is dead or not |
| [Vector3](Vector3.md) <b>Position</b> | Player's position in the game world |
| number <b>Speed</b> | Player's speed power value |
| number <b>BombPower</b> | Player's blast radius power value |
| number <b>Bombs</b> | Player's current bomb count (excludes placed bombs) |
| number <b>BombsTotal</b> | Player's current bomb count (includes placed bombs) |
| bool <b>HasPushing</b> | Whether the player has the Pushing powerup |
| bool <b>HasJumping</b> | Whether the player has the Jumping powerup |
| [ShieldState](ShieldState.md) <b>ShieldState</b> | State of the player's shield |
| number <b>Wins</b> | How many rounds were won by that player |
| number <b>Kills</b> | How many kills that player has |
| number <b>Deaths</b> | How many times that player died |
| [Team](Team.md) <b>Team</b> | The team this player is on |