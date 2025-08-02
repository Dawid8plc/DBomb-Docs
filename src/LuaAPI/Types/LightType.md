# LightType

Enumeration that represents the different light types that can be used on the [Light](../Tiles/Light.md) tile.

## Values
| | |
| -------- | ------- |
| <b>Spot</b> [0]  | The light is a cone-shaped spot light |
| <b>Directional</b> [1]  | The light is a directional light |
| <b>Point</b> [2]  | The light is a point light |

## Examples
```lua
local spotLight = LightType.Spot;

local directionalLight = LightType.Directional;

local pointLight = LightType.Point;
```