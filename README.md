# qb-lumberjack

Lumberjack job for QBCore: cut wood at the forest, process it into planks and
sell them to the wood seller.

## The loop

1. **Cut wood** at the marked trees → `wood` items
2. **Process** wood at the saw → `wood_pro` planks
3. **Sell** planks to the wood seller for cash

[Preview video](https://youtu.be/PnPM54h0ltI)

## Requirements

- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-target](https://github.com/qbcore-framework/qb-target)
- [qb-menu](https://github.com/qbcore-framework/qb-menu) (seller menu)
- A qb inventory fork using `inventory:client:ItemBox`

## Installation

1. Copy the resource into your `resources` folder and add to `server.cfg`:

```cfg
ensure qb-lumberjack
```

2. Copy the images from `images/` into your inventory resource's item images folder.

3. Add the items to `qb-core/shared/items.lua`:

```lua
["wood"]      = { name = "wood",      label = "Wood",         weight = 1000, type = "item", image = "wood.png",      unique = false, useable = false, shouldClose = false, combinable = nil, description = "Wood" },
["wood_cut"]  = { name = "wood_cut",  label = "Cut Wood",     weight = 1000, type = "item", image = "wood_cut.png",  unique = false, useable = false, shouldClose = false, combinable = nil, description = "Wood" },
["wood_pro"]  = { name = "wood_pro",  label = "Polish Wood",  weight = 1000, type = "item", image = "wood_proc.png", unique = false, useable = false, shouldClose = false, combinable = nil, description = "Wood" },
```

## Configuration

`config.lua` holds tree/process/seller locations + blips, sale prices and the
notification strings.

## License

All rights reserved.
