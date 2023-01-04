# ItemObjects

Items or objects (including creatures) that can be placed in locations.

## Declaration

To declare an ItemObject, start a line with `item` or `object`, followed by its ID, like so:

```
item gold_coin:
```

Colons and periods at the end of a line are ignored.

Keep in mind that the ID of the item will not be displayed to the player.


### Naming

To declare the name of the item shown to the player, use `called` or `or called` followed by the name.
The first name will be used when the game references the item. For example:


```
item gold_coin:
    called golden coin
    or called coin
    or called gold
```

The game will say

```
You see: 1 golden coin.
```

when there is a coin in the location.

### MultiItems

The plural name can be defined with `plural is`, like so:

```
item gold_coin:
    called golden coin
    or called coin
    or called gold
    plural is golden coins
```

This way, where there are multiple of the item, the game will show

```
You see: 5 golden coins.
```

To allow an item to have multiple instances, add `multiple` as a tag to the item.

```
item gold_coin:
    called golden coin
    or called coin
    or called gold
    plural is golden coins
    multiple
```

### Placement

To place a normal item in a location, add `in {location}` to the item declaraion. (Note: This cannot be used on items marked `multiple`.)

```
item gold_coin:
    called golden coin
    or called coin
    or called gold
    in vault
```



To place an item marked `multiple`, use `{amount} in {location}`. (Note: This can only be used on items marked `multiple`.)

```
item gold_coin:
    called golden coin
    or called coin
    or called gold
    plural is golden coins
    multiple
    5 in vault
```


### Collection

An item normally cannot be collected. To mark it as collectable, use `collectable`, `takeable`, or `get`.