# LaserReceiver

## Properties
| | |
| -------- | ------- |
| [Color](../Types/Color.md) <b>Color</b> | The color of the LaserReceiver when it is inactive |
| [Color](../Types/Color.md) <b>ActiveColor</b> | The color of the LaserReceiver when it is active |
| number <b>RequiredLaserCount</b> | How many lasers are required to activate this receiver |
| bool <b>StopLaser</b> | Whether this LaserReceiver prevents the laser from travelling further |
| number <b>MaxCalls</b> | How many times this receiver can be activated |
| [Vector3](../Types/Vector3.md) <b>PositionOffset</b> | The position offset of the LaserReceiver |
| [Vector3](../Types/Vector3.md) <b>RotationOffset</b> | The rotation offset of the LaserReceiver |
| [Vector3](../Types/Vector3.md) <b>ConstantRotation</b> | The speed of constant rotation on all three axes |
| bool <b>DontApplyPositionOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from moving to its original position upon using [ModTile](../WorldAPI/ModTile.md) |
| bool <b>DontApplyRotationOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from rotating to its original rotation upon using [ModTile](../WorldAPI/ModTile.md) |

## Actions
| | |
| -------- | ------- |
| <b>Reset</b> | Stops the LaserReceiver if its currently executing any actions and resets how many times it has been activated |