# TileLocation

Object that represents a position of a tile, relative or not.

## Constructors
<b>TileLocation</b>(number <b>X</b>, number <b>Y</b>, number <b>Layer</b>, bool <b>RelativePosition</b>)


## Properties
| | |
| -------- | ------- |
| number <b>X</b>  | X position of the tile |
| number <b>Y</b> | Y position of the tile |
| number <b>Layer</b>  | Layer on which the tile is located |
| bool <b>RelativePosition</b> | Whether relative positioning is used |

## Examples
```lua
local tileLoc = TileLocation(2, 2, 0, false);
```