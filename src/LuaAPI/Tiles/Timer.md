# Timer

## Properties
| | |
| -------- | ------- |
| number <b>MaxCalls</b> | How many times this Timer can be triggered |
| number <b>Delay</b> | The <b>Delay</b> until the Timer runs <b>OnEnter</b> on the target TriggerZone |
| [TileLocation](../Types/TileLocation.md) <b>TargetLoc</b> | The tile location of the target TriggerZone tile |
| [TimerTrigger](../Types/TimerTrigger.md) <b>Trigger</b> | The game event that should trigger this Timer automatically |

## Actions
| | |
| -------- | ------- |
| <b>Start</b> | Triggers the Timer |
| <b>Reset</b> | Stops the Timer if its currently running and resets how many times it has been triggered |
