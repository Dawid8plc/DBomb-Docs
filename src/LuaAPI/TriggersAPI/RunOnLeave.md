# [Triggers](../Triggers.md).RunOnLeave

## Declaration
[Triggers](../Triggers.md).<b>RunOnLeave</b>([Tile](../Types/Tile.md) <b>Trigger</b>)

## Description
Runs <b>OnLeave</b> on the provided <b>Trigger</b> tile, which can be either a TriggerZone or a ButtonTile.

```lua
--Gets the tile object for the TriggerZone and runs its OnLeave actions
local targetTrigger = World.GetTile(V2(4, 2), 0);

Triggers.RunOnLeave(targetTrigger);
```

---

## Declaration
[Triggers](../Triggers.md).RunO<b>RunOnLeave</b>nLeave([Tile](../Types/Tile.md) <b>Trigger</b>, [Player](../Types/Player.md) <b>Initiator</b>)

## Description
Runs <b>OnLeave</b> on the provided <b>Trigger</b> tile, which can be either a TriggerZone or a ButtonTile and passes the <b>Initiator</b> player.

```lua
--Gets the tile object for the TriggerZone and runs its OnLeave actions
--with the first player as the initiator
local players = Players.GetAll();
local player = players[1];
local targetTrigger = World.GetTile(V2(4, 2), 0);

Triggers.RunOnLeave(targetTrigger, player);
```

---

## Declaration
[Triggers](../Triggers.md).<b>RunOnLeave</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>Triggers</b>)

## Description
Runs <b>OnLeave</b> on the provided <b>Triggers</b> tiles, which can be either TriggerZone or a ButtonTiles.

```lua
--Gets the tile objects for the TriggerZones and runs their OnLeave actions
local targetTriggers = {World.GetTile(V2(4, 2), 0), World.GetTile(V2(4, 4), 0), World.GetTile(V2(4, 0), 0)};

Triggers.RunOnLeave(targetTriggers);
```

---

## Declaration
[Triggers](../Triggers.md).<b>RunOnLeave</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>Triggers</b>, [Player](../Types/Player.md) <b>Initiator</b>)

## Description
Runs <b>OnLeave</b> on the provided <b>Triggers</b> tiles, which can be either TriggerZone or a ButtonTiles and passes the <b>Initiator</b> player.

```lua
--Gets the tile objects for the TriggerZones and runs their OnLeave actions
--with the first player as the initiator
local players = Players.GetAll();
local player = players[1];
local targetTriggers = {World.GetTile(V2(4, 2), 0), World.GetTile(V2(4, 4), 0), World.GetTile(V2(4, 0), 0)};

Triggers.RunOnLeave(targetTriggers, player);
```