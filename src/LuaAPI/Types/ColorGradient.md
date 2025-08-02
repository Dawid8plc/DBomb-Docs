# ColorGradient

Object that represents a color gradient. 

Each color gradient consists of several colors and alphas (max is 8 for both).

The <b>Time</b> property on the keys has to be between 0 and 1.

<b>Alpha</b> is in the range of 0 to 255.

## Constructors
<b>ColorGradient</b>()


## Functions
| | |
| -------- | ------- |
| <b>AddColor</b>([ColorKey](ColorKey.md) <b>Key</b>)  | Adds a color key to the gradient (max is 8) |
| <b>AddColor</b>([Color](Color.md) <b>Color</b>, number <b>Time</b>) | Creates a color key with the given parameters and adds it (max is 8) |
| [ColorKey](ColorKey.md) <b>GetColor</b>(number <b>Index</b>) | Returns the color key on the given <b>Index</b> |
| <b>RemoveColor</b>(number <b>Index</b>) | Removes the color key on the given <b>Index</b> |
| <b>AddAlpha</b>([AlphaKey](AlphaKey.md) <b>Key</b>)  | Adds an alpha key to the gradient (max is 8) |
| <b>AddAlpha</b>([number <b>Alpha</b>, number <b>Time</b>) | Creates an alpha key with the given parameters and adds it (max is 8) |
| [AlphaKey](AlphaKey.md) <b>GetAlpha</b>(number <b>Index</b>) | Returns the alpha key on the given <b>Index</b> |
| <b>RemoveAlpha</b>(number <b>Index</b>) | Removes the alpha key on the given <b>Index</b> |

## Examples
```lua
local colorGradient = ColorGradient();
colorGradient.AddColor(Color(252, 186, 3, 255), 0);
colorGradient.AddColor(Color(45, 252, 3, 255), 0.5);
colorGradient.AddColor(Color(98, 3, 252, 255), 1);
colorGradient.AddAlpha(255, 0);
colorGradient.AddAlpha(255, 1);
```