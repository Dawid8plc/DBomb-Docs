# Light

## Properties
| | |
| -------- | ------- |
| bool <b>Enabled</b> | Whether this Light tile is currently emitting light |
| [LightType](../Types/LightType.md) <b>Type</b> | The type of this Light. Default is <b>Point</b> |
| [LightModel](../Types/LightModel.md) <b>Model</b> | The 3D model of this Light. Default is <b>Modern</b> |
| [Color](../Types/Color.md) <b>Color</b> | The color of the emitted light |
| number <b>Intensity</b> | The intensity of the emitted light |
| number <b>Range</b> | The range of the emitted light, only used when <b>Type</b> is set to <b>Spot</b> and <b>Point</b> |
| number <b>OuterSpotAngle</b> | The outer angle in degrees, at the base of a Spot light's cone. Only used when <b>Type</b> is set to <b>Spot</b> |
| number <b>InnerSpotAngle</b> | The inner angle in degrees, at the base of a Spot light's cone. Only used when <b>Type</b> is set to <b>Spot</b> |
| [Vector3](../Types/Vector3.md) <b>PositionOffset</b> | The position offset of the Light |
| [Vector3](../Types/Vector3.md) <b>RotationOffset</b> | The rotation offset of the Light |
| [Vector3](../Types/Vector3.md) <b>ConstantRotation</b> | The speed of constant rotation on all three axes |
| bool <b>DontApplyPositionOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from moving to its original position upon using [ModTile](../WorldAPI/ModTile.md) |
| bool <b>DontApplyRotationOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the tile from rotating to its original rotation upon using [ModTile](../WorldAPI/ModTile.md) |