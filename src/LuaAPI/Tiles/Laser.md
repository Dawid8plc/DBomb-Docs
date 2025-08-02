# Laser

## Properties
| | |
| -------- | ------- |
| bool <b>Enabled</b> | Whether the Laser emitter is enabled |
| [ColorGradient](../Types/ColorGradient.md) <b>LaserGradient</b> | The color gradient of the Laser |
| [Color](../Types/Color.md) <b>Color</b> | The color gradient of the orb around the Laser emitter |
| number <b>Thickness</b> | Thickness of the Laser |
| number <b>Range</b> | Range of the Laser |
| [Vector3](../Types/Vector3.md) <b>PositionOffset</b> | The position offset of the Laser emitter |
| [Vector3](../Types/Vector3.md) <b>RotationOffset</b> | The rotation offset of the Laser emitter |
| [Vector3](../Types/Vector3.md) <b>ConstantRotation</b> | The speed of constant rotation on all three axes |
| bool <b>DontApplyPositionOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from moving to its original position upon using [ModTile](../WorldAPI/ModTile.md) |
| bool <b>DontApplyRotationOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from rotating to its original rotation upon using [ModTile](../WorldAPI/ModTile.md) |