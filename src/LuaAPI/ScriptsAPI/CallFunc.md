# [Scripts](../Scripts.md).CallFunc

## Declaration
[Scripts](../Scripts.md).<b>CallFunc</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>, string <b>FunctionName</b>)

## Description
Calls function with name <b>FunctionName</b> on <b>ScriptTile</b> and returns the value returned by it. Function doesn't have to be editor-defined, nor does it have to return anything.

```lua
--This function is defined in another script, Score is an editor-defined variable
function GetScore()
    return Score;
end

--Gets the Tile object of the other ScriptTile,
--then calls the "GetScore" function on its Script,
--Then prints the returned value in the Scripts Console
local otherScriptTile = World.GetTile(V2(4, 5), 0);
local score = Scripts.CallFunc(otherScriptTile, "GetScore");

Print(score);
```

---

## Declaration
[Scripts](../Scripts.md).<b>CallFunc</b>([Tile](../Types/Tile.md) <b>ScriptTile</b>, string <b>FunctionName</b>, Dictionary <b>Parameters</b>)

## Description
Calls function with name <b>FunctionName</b> on <b>ScriptTile</b> with the provided <b>Parameters</b> and returns the value returned by it. Function doesn't have to be editor-defined, nor does it have to return anything.

```lua
--These functions are defined in another script, Score is an editor-defined variable
function GetScore()
    return Score;
end

function AddScore(value)
    Score = Score + value;
end

--Gets the Tile object of the other ScriptTile,
--then calls the "AddScore" function on its Script, along with a parameter
--then prints the updated score in the Scripts Console
local otherScriptTile = World.GetTile(V2(4, 5), 0);
local params = {20};
Scripts.CallFunc(otherScriptTile, "AddScore", params);

local score = Scripts.CallFunc(otherScriptTile, "GetScore");

Print(score);
```

---

## Declaration
[Scripts](../Scripts.md).<b>CallFunc</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>, string <b>FunctionName</b>)

## Description
Calls function with name <b>FunctionName</b> on <b>ScriptTiles</b> and returns the values returned by them in the form of a Dictionary. Function doesn't have to be editor-defined, nor does it have to return anything.

```lua
--This function is defined in another script, Score is an editor-defined variable
function GetScore()
    return Score;
end

--Gets the Tile objects of the other ScriptTiles,
--then calls the "GetScore" function on their Scripts,
--then prints all the scores in the Scripts Console
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
local scores = Scripts.CallFunc(otherScriptTiles, "GetScore");

for i, score in ipairs(scores) do 
    Print("Score #" .. i .. ": " .. score);
end

--Prints the score of the second ScriptTile
Print("Score #2: " .. scores[2]);
```

---

## Declaration
[Scripts](../Scripts.md).<b>CallFunc</b>(Dictionary\<[Tile](../Types/Tile.md)> <b>ScriptTiles</b>, string <b>FunctionName</b>, Dictionary <b>Parameters</b>)

## Description
Calls function with name <b>FunctionName</b> on <b>ScriptTiles</b> with the provided <b>Parameters</b> and returns the values returned by them in the form of a Dictionary. Function doesn't have to be editor-defined, nor does it have to return anything.

```lua
--These functions are defined in another script, Score is an editor-defined variable
function GetScore()
    return Score;
end

function AddScore(value)
    Score = Score + value;
end

--Gets the Tile objects of the other ScriptTiles,
--then calls the "AddScore" function on their Scripts, along with a parameter
--then prints all the updated scores in the Scripts Console
local otherScriptTiles = {World.GetTile(V2(4, 5), 0), World.GetTile(V2(2, 5), 0), World.GetTile(V2(0, 5), 0)};
local params = {20};
Scripts.CallFunc(otherScriptTiles, "AddScore", params);

local scores = Scripts.CallFunc(otherScriptTiles, "GetScore");

for i, score in ipairs(scores) do 
    Print("Score #" .. i .. ": " .. score);
end
```