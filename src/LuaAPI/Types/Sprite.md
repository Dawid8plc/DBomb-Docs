# Sprite

Object that represents a 2D sprite.

## Constructors
<b>Sprite</b>(string <b>ID</b>, [Color](Color.md) <b>Color</b>)

## Properties
| | |
| -------- | ------- |
| string <b>ID</b>  | ID of the sprite |
| [Color](Color.md) <b>Color</b> | Color of the sprite |

## Examples
```lua
local blankSprite = Sprite("Blank", Color(255, 255, 255, 255));

local bombSprite = Sprite("Bomb", Color(255, 255, 255, 255));

local redTriangle = Sprite("Shape Triangle", Color(255, 0, 0, 255));
```