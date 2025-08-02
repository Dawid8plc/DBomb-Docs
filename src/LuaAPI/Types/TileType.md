# TileType

Enumeration that represents the different tile types in the game.

## Values
| | |
| -------- | ------- |
| <b>Air</b> [0]  | The Air tile |
| <b>Floor</b> [1]  | The Floor tile |
| <b>Spawnpoint</b> [2]  | The Spawnpoint tile |
| <b>Wall</b> [3]  | The Wall tile |
| <b>SDWall</b> [4]  | The Sudden Death Wall tile |
| <b>Crate</b> [5]  | The Crate tile |
| <b>MetalCrate</b> [6]  | The Metal Crate tile |
| <b>Teleporter</b> [7]  | The Teleporter tile |
| <b>Spikes</b> [8]  | The Spikes tile |
| <b>CountBomb</b> [9]  | The Count Bomb tile |
| <b>CrateBomb</b> [10]  | The Crate Bomb tile |
| <b>LandMine</b> [11]  | The Land Mine tile |
| <b>PowerupTile</b> [12]  | The Powerup tile |
| <b>InfoTile</b> [13]  | The Info tile |
| <b>Fuse</b> [14]  | The Fuse tile |
| <b>BombField</b> [15]  | The Bomb Field tile |
| <b>Slope</b> [16]  | The Slope tile |
| <b>Pusher</b> [17]  | The Pusher tile |
| <b>Launcher</b> [18]  | The Launcher tile |
| <b>Button</b> [19]  | The Button tile |
| <b>TriggerZone</b> [20]  | The Trigger Zone tile |
| <b>Timer</b> [21]  | The Timer tile |
| <b>Symbol</b> [22]  | The Symbol tile|
| <b>Text</b> [23]  | The Text tile |
| <b>Ice</b> [24]  | The Ice tile |
| <b>Collectible</b> [25]  | The Collectible tile |
| <b>CustomWall</b> [26]  | The Custom Wall tile |
| <b>Laser</b> [27]  | The Laser tile |
| <b>LaserMirror</b> [28]  | The Laser Mirror tile |
| <b>ScriptTile</b> [29]  | The Script tile |
| <b>LaserBarrier</b> [30]  | The Laser Barrier tile |
| <b>LaserRelay</b> [31]  | The Laser Relay tile |
| <b>LaserReceiver</b> [32]  | The Laser Receiver tile |
| <b>Breakable</b> [33]  | The Breakable tile |
| <b>Light</b> [34]  | The Light tile |
| <b>CornerSlope</b> [35]  | The Corner Slope tile |

## Examples
```lua
local crateType = TileType.Crate;

local laserTile = TileType.Laser;

local pusherTile = TileType.Pusher;
```