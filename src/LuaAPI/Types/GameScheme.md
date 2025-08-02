# GameSheme

Object that represents the match settings, or otherwise known as game scheme or rules.

## Properties
| | |
| -------- | ------- |
| string <b>Name</b>  | Name of the scheme |
| number <b>StartingBombs</b>  | Number of starting Bombs |
| number <b>StartingPower</b>  | Number of starting Blast Radius |
| number <b>StartingSpeed</b>  | Number of starting Speed |
| bool <b>StartShielded</b>  | Whether players start with the Shield powerup |
| bool <b>StartPushing</b>  | Whether players start with the Pushing powerup |
| bool <b>StartJumping</b>  | Whether players start with the Jumping powerup |
| bool <b>PreservePowerups</b>  | Whether preserving powerups is enabled |
| bool <b>PreserveBombs</b>  | Whether preserving Bombs is enabled |
| bool <b>PreserveBlastRadius</b>  | Whether preserving Blast Radius is enabled |
| bool <b>PreserveSpeed</b>  | Whether preserving Speed is enabled |
| bool <b>PreserveShield</b>  | Whether preserving Shield is enabled |
| bool <b>PreservePushing</b>  | Whether preserving Pushing is enabled |
| bool <b>PreserveJumping</b>  | Whether preserving Jumping is enabled |
| number <b>DropChance</b>  | The chance to drop a powerup from a crate, from 0 to 100 |
| number <b>BombsDropRate</b>  | Drop rate of the Bomb powerup, from 0 to 5 |
| number <b>PowerDropRate</b>  | Drop rate of the Blast Radius powerup, from 0 to 5 |
| number <b>SpeedDropRate</b>  | Drop rate of the Speed powerup, from 0 to 5 |
| number <b>ShieldDropRate</b>  | Drop rate of the Shield powerup, from 0 to 5 |
| number <b>PushDropRate</b>  | Drop rate of the Pushing powerup, from 0 to 5 |
| number <b>JumpDropRate</b>  | Drop rate of the Jumping powerup, from 0 to 5 |
| bool <b>SixWayExplosions</b>  | Whether six way explosions are enabled |
| bool <b>ImpactBombs</b>  | Whether bombs explode on impact is enabled |
| bool <b>Darkness</b>  | Whether darkness is enabled |
| number <b>Rounds</b>  | Number of rounds to be played |
| number <b>SuddenDeathMinutes</b>  | Minutes until Sudden Death starts |
| [GameMode](../Types/GameMode.md) <b>GameMode</b>  | The selected game mode |