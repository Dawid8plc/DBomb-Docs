# TriggerZone

## Properties
| | |
| -------- | ------- |
| [Vector3](../Types/Vector3.md) <b>PositionOffset</b> | Position offset of the <b>TriggerZone</b> |
| number <b>SizeX</b> | The size of the TriggerZone on the X axis |
| number <b>SizeY</b> | The size of the TriggerZone on the Y axis |
| number <b>SizeZ</b> | The size of the TriggerZone on the Z axis |
| number <b>MaxCalls</b> | How many times this TriggerZone can be triggered |
| number <b>SeparateMaxCalls</b> | Whether players should have separate <b>MaxCalls</b> |
| bool <b>PlayerTrigger</b> | Whether players can trigger this TriggerZone |
| bool <b>BombTrigger</b> | Whether bombs can trigger this TriggerZone |
| bool <b>ExplosionTrigger</b> | Whether explosions can trigger this TriggerZone |
| bool <b>TriggerExplosionTrigger</b> | Whether explosions spawned by triggers or scripts can trigger this TriggerZone |
| bool <b>RunOnEveryEnterLeave</b> | Whether the <b>OnEnter</b> and <b>OnLeave</b> actions should be ran every single time a player enters or leaves the TriggerZone, or only when a player enters when there are no other players inside it, or when the last player leaves |
| bool <b>DontApplyPositionOffset</b> | Special, made to be passed using [ModTile](../WorldAPI/ModTile.md). Prevents the TriggerZone from moving to its original position upon using [ModTile](../WorldAPI/ModTile.md) |

## Actions
| | |
| -------- | ------- |
| <b>Reset</b> | Stops the TriggerZone if its currently executing any actions and resets how many times it has been triggered |