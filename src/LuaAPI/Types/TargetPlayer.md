# TargetPlayer

Enumeration that represents the targeting mode in various functions of this API. Usually passed along with the ID of the target player, and a [Vector3](Vector3.md) as a point of reference.

## Values
| | |
| -------- | ------- |
| <b>Initiator</b> [0]  | Targets the target player|
| <b>Everyone</b> [1]  | Targets everyone |
| <b>Others</b> [2]  | Targets everyone but the target player |
| <b>Random</b> [3]  | Targets a random player |
| <b>Closest</b> [4]  | Targets the closest player to the point of reference |
| <b>Furthest</b> [5]  | Targets the furthest player to the point of reference |
| <b>AllTeamMembers</b> [6]  | Targets all the team members of the target player, target player included |
| <b>OtherTeamMembers</b> [7]  | Targets all the team members of the target player, target player excluded |
| <b>OtherTeams</b> [8]  | Targets all the other teams, which target player is not part of |

## Examples
```lua
local initiator = TargetPlayer.Initiator;

local others = TargetPlayer.Others;

local everyone = TargetPlayer.Everyone;
```