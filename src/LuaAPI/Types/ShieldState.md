# ShieldState

Enumeration that represents the different states of the player's shield.

## Values
| | |
| -------- | ------- |
| <b>Active</b> [0]  | The shield is active |
| <b>Damaged</b> [1]  | The shield is damaged, and about to enter inactive state |
| <b>Inactive</b> [2]  | The shield is inactive |

## Examples
```lua
local activeShieldState = ShieldState.Active;

local damagedShieldState = ShieldState.Damaged;

local inactiveShieldState = ShieldState.Inactive;
```