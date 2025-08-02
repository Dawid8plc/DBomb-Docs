# Button

## Properties
| | |
| -------- | ------- |
| number <b>MaxCalls</b> | How many times this button can be triggered |
| number <b>SeparateMaxCalls</b> | Whether players should have separate <b>MaxCalls</b> |
| [Color](../Types/Color.md) <b>RepeatingStyle</b> | The color of this Button |
| bool <b>PlayerTrigger</b> | Whether players can trigger this button |
| bool <b>BombTrigger</b> | Whether bombs can trigger this button |
| bool <b>ExplosionTrigger</b> | Whether explosions can trigger this button |
| bool <b>TriggerExplosionTrigger</b> | Whether explosions spawned by triggers or scripts can trigger this button |

## Actions
| | |
| -------- | ------- |
| <b>Reset</b> | Stops the Button if its currently executing any actions and resets how many times it has been triggered |