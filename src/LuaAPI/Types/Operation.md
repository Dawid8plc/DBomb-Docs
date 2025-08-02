# Operation

Enumeration that represents the operation mode in various functions of this API. Usually used when adding, subtracting or setting values.

## Values
| | |
| -------- | ------- |
| <b>Add</b> [0]  | Indicates that the values should be added |
| <b>Subtract</b> [1]  | Indicates that the values should be subtracted |
| <b>Set</b> [2]  | Indicates that the values should be set |

## Examples
```lua
local add = Operation.Add;

local subtract = Operation.Subtract;

local set = Operation.Set;
```