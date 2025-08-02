# [Scripts](../Scripts.md).GetVar

## Declaration
[Scripts](../Scripts.md).<b>GetVar</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>)

## Description
Returns all the variables from a <b>ScriptTile</b> in the form of a Dictionary.

```lua
--Gets the Tile object of the other ScriptTile, 
--and gets all the editor-exposed variables from it,
--then prints them in the Scripts Console
local otherScriptTile = World.GetTile(V2(4, 5), 0);
local variables = Scripts.GetVar(otherScriptTile);

for name, value in pairs(variables) do 
    Print(name .. ": " .. tostring(value));
end

--Prints a specific variable in the Scripts Console
Print("BlastForce: " .. variables["BlastForce"]);
```

---

## Declaration
[Scripts](../Scripts.md).<b>GetVar</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>, string <b>Name</b>)

## Description
Returns the value of the <b>Name</b> variable from a <b>ScriptTile</b>.

```lua
--Gets the Tile object of the other ScriptTile, and gets the value of 
--the editor-exposed "BlastForce" variable then prints it in the Scripts Console
local otherScriptTile = World.GetTile(V2(4, 5), 0);
local force = Scripts.GetVar(otherScriptTile, "BlastForce");

Print(force);
```

---

## Declaration
[Scripts](../Scripts.md).<b>GetVar</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>)

## Description
Returns all the variables from <b>ScriptTiles</b> in the form of a Dictionary of dictionaries.

```lua
--Gets the Tile objects of the other ScriptTiles, 
--and gets all the editor-exposed variables from them, 
--then prints them in the Scripts Console
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
local scripts = Scripts.GetVar(otherScriptTiles);

for i, scriptVars in ipairs(scripts) do 
    for name, value in pairs(scriptVars) do 
        Print("Script Tile #" .. i .. " " .. name .. ": " .. tostring(value));
    end
end

--Prints a specific variable from a specific ScriptTile in the Scripts Console
Print("Script Tile #2 BlastForce: " .. scripts[2]["BlastForce"]);
```

---

## Declaration
[Scripts](../Scripts.md).<b>GetVar</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>, string <b>Name</b>)

## Description
Returns the values of the <b>Name</b> variable from <b>ScriptTiles</b> in the form of a Dictionary.

```lua
--Gets the Tile objects of the other ScriptTiles, 
--and gets all the editor-exposed "BlastForce" variables then prints them in the Scripts Console
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
local forces = Scripts.GetVar(otherScriptTiles, "BlastForce");

for i, force in ipairs(forces) do 
    Print("Script Tile #" .. i .. " BlastForce: " .. force);
end

--Prints a specific "BlastForce" from a specific ScriptTile in the Scripts Console
Print("Script Tile #2 BlastForce: " .. forces[2]);
```
