# Color
Object that represents colors using RGBA.

Each component is a number from range 0 to 255.

## Constructors
<b>Color</b>(number <b>R</b>, number <b>G</b>, number <b>B</b>, number <b>A</b>)


## Properties
| | |
| -------- | ------- |
| number <b>r</b>  | Red component of the color |
| number <b>g</b> | Green component of the color |
| number <b>b</b> | Blue component of the color |
| number <b>a</b> | Alpha component of the color |

## Examples
```lua
local red = Color(255, 0, 0, 255);
local green = Color(0, 255, 0, 255);
local blue = Color(0, 0, 255, 255);
```