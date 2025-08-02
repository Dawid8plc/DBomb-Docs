# ColorKey

Object that represents a color key in a gradient, that consists of a <b>Color</b> and a <b>Time</b> property.

The <b>Time</b> property has to be between 0 and 1.

## Constructors
<b>ColorKey</b>([Color](Color.md) <b>Color</b>, number <b>Time</b>)

## Functions
| | |
| -------- | ------- |
| [Color](Color.md) <b>Color</b>| The color in this key |
| number <b>Time</b>| The time in this key |

## Examples
```lua
local aquaColorKey = ColorKey(Color(0, 255, 255, 255), 0);
```