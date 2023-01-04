# Locations

Locations are places where the player can be in. The player cannot move within a location, only go to another location from this one.

## Declaration

To declare a location, use `location`, like so:


```
location name
```

### Idle text
<div id="idle text"></div>

When the player is in the location, an idle text will be chosen at random from the list. To declare an idle text, use any of the following:

```
location name
    in name, say "Idle text"
    in name say "Idle text"
    in it, say "Idle text"
    in it say "Idle text"
    in here, say "Idle text"
    in here say "Idle text"
    in there, say "Idle text"
    in there say "Idle text"
    or say "Idle text"
```

The keywords `say`, `says`, `respond`, `responds`, `report`, and `reports` are interchangable.

Note that `or say` can only by used after declaring once using any other method. This is to prevent conflicts with [search text](#search text).


### Search text
<div id="search text"></div>

Searching the room will return a random search text from the list of defined search texts. To declare search text, use any of the following:

```
location name
    searching name say "You search the room."
    searching it say "You search the room."
    searching here say "You search the room."
    searching there say "You search the room."
    or say "You search the room."
```

The keywords `say`, `says`, `respond`, `responds`, `report`, and `reports` are interchangable.
Note that `or say` can only by used after declaring once using any other method. This is to prevent conflicts with [idle text](#idle text).

### Starting location

To set the location as the starting location, use `start here`.

This will cause the player to be in this location at the start of the game. In case of multiple starting locations defined, 
the last starting location defined will be the starting location.


### Exits

Exits are ways for the player to move from location to location. Each location can have 10 exits, their aliases can be found [here](./exitlst).

To declare an exit, use `to the <dir> is <loc>`, where `<dir>` is the direction, and `<loc>` is the location of where that direciton leads.

To change exits at runtime, see changing [exits at runtime](/script/objects/Functions/#runtime-exits).