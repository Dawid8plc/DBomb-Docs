# [Triggers](../Triggers.md).AddOnLeaveHandler

## Declaration
[Triggers](../Triggers.md).<b>AddOnLeaveHandler</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, function <b>Handler</b>)

## Description
Creates a special Call Function Script trigger action, that calls the <b>Handler</b> function and then adds it to the TriggerZone or Button tile's <b>OnLeave</b> at <b>Position</b> on <b>Layer</b>. This causes the aforementioned tile types to run the <b>Handler</b> function upon being left or otherwise triggered.

```lua
function GiveBomb(Tile, Player)
    --The Tile parameter is the Tile object for the tile that ran this function
    --So either the Button or TriggerZone tile.

    --The Player parameter is the Player object, if applicable, of the player that triggered the above tiles
    --So for example the player that walked onto the button

    --Its possible for the Player variable to be nil

    if Player ~= nil then
        local container = Powerups();
        container.Bombs = 1;

        Players.SetPowerups(Player, container, Operation.Add);
    end
end

--Adds a handler to the Button which causes it to run the GiveBomb function
--What's important is that the GiveBomb function will be ran on this ScriptTile, and will have access to its variables
local buttonPos = V2(7, 7);
local buttonLayer = 1;
Triggers.AddOnLeaveHandler(buttonPos, buttonLayer, GiveBomb);
```

---

## Declaration
[Triggers](../Triggers.md).<b>AddOnLeaveHandler</b>([Vector2](../Types/Vector2.md) <b>Position</b>, number <b>Layer</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>, function <b>Handler</b>)

## Description
Creates a special Call Function Script trigger action, that calls the <b>Handler</b> function and then adds it to the TriggerZone or Button tile's <b>OnLeave</b> at <b>Position</b> on <b>Layer</b>. This causes the aforementioned tile types to run the <b>Handler</b> function upon being left or otherwise triggered. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
function GiveBomb(Tile, Player)
    --The Tile parameter is the Tile object for the tile that ran this function
    --So either the Button or TriggerZone tile.

    --The Player parameter is the Player object, if applicable, of the player that triggered the above tiles
    --So for example the player that walked onto the button

    --Its possible for the Player variable to be nil

    if Player ~= nil then
        local container = Powerups();
        container.Bombs = 1;

        Players.SetPowerups(Player, container, Operation.Add);
    end
end

--Adds a handler to the Button which causes it to run the GiveBomb function
--What's important is that the GiveBomb function will be ran on this ScriptTile, and will have access to its variables
local buttonRelativePos = V2(2, 2);
local buttonLayer = 1;
local origin = V2(5, 5);
Triggers.AddOnLeaveHandler(buttonRelativePos, buttonLayer, true, origin, GiveBomb);
```

---

## Declaration
[Triggers](../Triggers.md).<b>AddOnLeaveHandler</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, function <b>Handler</b>)

## Description
Creates a special Call Function Script trigger action, that calls the <b>Handler</b> function and then adds it to the TriggerZone or Button tiles <b>OnLeave</b> at <b>Positions</b> on <b>Layer</b>. This causes the aforementioned tile types to run the <b>Handler</b> function upon being left or otherwise triggered. <b>Position</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
function GiveBomb(Tile, Player)
    --The Tile parameter is the Tile object for the tile that ran this function
    --So either the Button or TriggerZone tile.

    --The Player parameter is the Player object, if applicable, of the player that triggered the above tiles
    --So for example the player that walked onto the button

    --Its possible for the Player variable to be nil

    if Player ~= nil then
        local container = Powerups();
        container.Bombs = 1;

        Players.SetPowerups(Player, container, Operation.Add);
    end
end

--Adds a handler to the Buttons which causes it to run the GiveBomb function
--What's important is that the GiveBomb function will be ran on this ScriptTile, and will have access to its variables
local buttons = {V2(7, 7), V2(7, 5), V2(9, 7), V2(9, 5)};
local buttonLayer = 1;
Triggers.AddOnLeaveHandler(buttons, buttonLayer, GiveBomb);
```

---

## Declaration
[Triggers](../Triggers.md).<b>AddOnLeaveHandler</b>(Dictionary\<[Vector2](../Types/Vector2.md)> <b>Positions</b>, number <b>Layer</b>, bool <b>Relative</b>, [Vector2](../Types/Vector2.md) <b>Origin</b>, function <b>Handler</b>)

## Description
Creates a special Call Function Script trigger action, that calls the <b>Handler</b> function and then adds it to the TriggerZone or Button tiles <b>OnLeave</b> at <b>Positions</b> on <b>Layer</b>. This causes the aforementioned tile types to run the <b>Handler</b> function upon being left or otherwise triggered. <b>Positions</b> can be relative to <b>Origin</b> if <b>Relative</b> parameter is <b>true</b>.

```lua
function GiveBomb(Tile, Player)
    --The Tile parameter is the Tile object for the tile that ran this function
    --So either the Button or TriggerZone tile.

    --The Player parameter is the Player object, if applicable, of the player that triggered the above tiles
    --So for example the player that walked onto the button

    --Its possible for the Player variable to be nil

    if Player ~= nil then
        local container = Powerups();
        container.Bombs = 1;

        Players.SetPowerups(Player, container, Operation.Add);
    end
end

--Adds a handler to the Buttons which causes it to run the GiveBomb function
--What's important is that the GiveBomb function will be ran on this ScriptTile, and will have access to its variables
local relativeButtons = {V2(-1, 1), V2(1, 1), V2(-1, -1), V2(1, -1)};
local buttonLayer = 1;
local origin = V2(8, 6);
Triggers.AddOnLeaveHandler(relativeButtons, buttonLayer, true, origin, GiveBomb);
```
