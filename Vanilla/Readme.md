# Vanilla Minecraft

## component.jukebox

Block: Juke Box

```Lua
address -- Address of device
type    jukebox
slot    -1

play    function() -- Start playing the record currently in the jukebox.

getRecord   function():string -- Get the title of the record currently in the jukebox.

stop    function() -- Stop playing the record currently in the jukebox.
```

## component.furnace

Block: Furnace

```Lua
address -- Address of device
type    furnace
slot    -1

getCookTime function():number -- The number of ticks that the current item has been cooking for.

isBurning   function():boolean -- Get whether the furnace is currently active.

getCurrentItemBurnTime  function():number -- The number of ticks that the currently burning fuel lasts in total.

getTotalCookTime    function():number -- The number of ticks that the current item needs to cook.

getBurnTime function():number -- The number of ticks that the furnace will keep burning from the last consumed fuel.
```

## component.note_block

Block: Note Block

```Lua
address -- Address of device
type    note_block
slot    -1

trigger function([pitch:number]):boolean -- Triggers the note block if possible. Allows setting the pitch for to save a tick.

setPitch    function(value:number) -- Set the pitch for this note block. Must be in the interval [1, 25].

getPitch    function():number -- Get the currently set pitch on this note block.
```

## component.comparator

Block: Redstone comparator

```Lua
address -- Address of device
type    comparator
slot    -1

getOutputSignal function():number -- Get the strength of the comparators output signal.
```