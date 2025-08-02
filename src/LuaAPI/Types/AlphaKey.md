# AlphaKey

Object that represents an alpha key in a gradient, that consists of an <b>Alpha</b> and a <b>Time</b> property.

The <b>Alpha</b> property has to be between 0 and 255.
The <b>Time</b> property has to be between 0 and 1.

## Constructors
<b>AlphaKey</b>(number <b>Alpha</b>, number <b>Time</b>)

## Functions
| | |
| -------- | ------- |
| number <b>Alpha</b>| The alpha in this key |
| number <b>Time</b>| The time in this key |

## Examples
```lua
local alphaKey = AlphaKey(255, 0);
```