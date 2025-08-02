# LaserRelay

## Properties
| | |
| -------- | ------- |
| [Color](../Types/Color.md) <b>Color</b> | The color of the LaserRelay |
| number <b>LasersCount</b> | How many lasers this relay outputs |
| number <b>AngleBetweenLasers</b> | The angle between outputted lasers |
| [Vector3](../Types/Vector3.md) <b>PositionOffset</b> | The position offset of the LaserRelay |
| [Vector3](../Types/Vector3.md) <b>RotationOffset</b> | The rotation offset of the LaserRelay |
| [Vector3](../Types/Vector3.md) <b>ConstantRotation</b> | The speed of constant rotation on all three axes |
| bool <b>DontApplyPositionOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from moving to its original position upon using [ModTile](../WorldAPI/ModTile.md) |
| bool <b>DontApplyRotationOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from rotating to its original rotation upon using [ModTile](../WorldAPI/ModTile.md) |