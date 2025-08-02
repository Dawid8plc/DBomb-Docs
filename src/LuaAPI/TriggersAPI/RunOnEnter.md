# [Triggers](../Triggers.md).RunOnEnter

## Declaration
[Triggers](../Triggers.md).<b>RunOnEnter</b>([Tile](../Types/Tile.md) <b>Trigger</b>)

## Description
Runs <b>OnEnter</b> on the provided <b>Trigger</b> tile, which can be either a TriggerZone or a ButtonTile.

```lua
--Gets the tile object for the TriggerZone and runs its OnEnter actions
local targetTrigger = World.GetTile(V2(4, 2), 0);

Triggers.RunOnEnter(targetTrigger);
```

---

## Declaration
[Triggers](../Triggers.md).<b>RunOnEnter</b>([Tile](../Types/Tile.md) <b>Trigger</b>, [Player](../Types/Player.md) <b>Initiator</b>)

## Description
Runs <b>OnEnter</b> on the provided <b>Trigger</b> tile, which can be either a TriggerZone or a ButtonTile and passes the <b>Initiator</b> player.

```lua
--Gets the tile object for the TriggerZone and runs its OnEnter actions
--with the first player as the initiator
local players = Players.GetAll();
local player = players[1];
local targetTrigger = World.GetTile(V2(4, 2), 0);

Triggers.RunOnEnter(targetTrigger, player);
```

---

## Declaration
[Triggers](../Triggers.md).<b>RunOnEnter</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>Triggers</b>)

## Description
Runs <b>OnEnter</b> on the provided <b>Triggers</b> tiles, which can be either TriggerZone or ButtonTiles.

```lua
--Gets the tile objects for the TriggerZones and runs their OnEnter actions
local targetTriggers = {World.GetTile(V2(4, 2), 0), World.GetTile(V2(4, 4), 0), World.GetTile(V2(4, 0), 0)};

Triggers.RunOnEnter(targetTriggers);
```

---

## Declaration
[Triggers](../Triggers.md).<b>RunOnEnter</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>Triggers</b>, [Player](../Types/Player.md) <b>Initiator</b>)

## Description
Runs <b>OnEnter</b> on the provided <b>Triggers</b> tiles, which can be either TriggerZone or ButtonTiles and passes the <b>Initiator</b> player.

```lua
--Gets the tile objects for the TriggerZones and runs their OnEnter actions
--with the first player as the initiator
local players = Players.GetAll();
local player = players[1];
local targetTriggers = {World.GetTile(V2(4, 2), 0), World.GetTile(V2(4, 4), 0), World.GetTile(V2(4, 0), 0)};

Triggers.RunOnEnter(targetTriggers, player);
```