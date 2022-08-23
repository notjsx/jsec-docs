# CF Documentation
You can only have one CF block per chunk, and you can not nest cf blocks.

## Initialize CF block
```lua
CF_START()
```

## End CF block
```lua
CF_END()
```

JSEC will then take all those blocks, attempt to randomize the flow of the statements within the block and output it at the block location.
