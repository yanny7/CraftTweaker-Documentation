# Mod configuration

## Package
`import mods.stone_age.ConfigManager;`

## Methods

### getDisabledBlocksInStoneAge
Get list of blocks that have disabled use (righ-click) until the player is in Stone Age (until he crafts Crafting Table)

Returns [MCBlock](/Vanilla/Blocks/MCBlock/)[]

```
MCBlock[] ConfigManager.getDisabledBlocksInStoneAge()

var blocks = ConfigManager.getDisabledBlocksInStoneAge()
```

### addDisabledBlockInStoneAge
Add blocks to list of disabled blocks that have disabled use.

- **String ...blockNames** list of block resource names

```
ConfigManager.addDisabledBlockInStoneAge(String ...blockNames);

ConfigManager.addDisabledBlockInStoneAge("minecraft:furnace", "minecraft:dispenser");
```

### removeDisabledBlockInStoneAge
Remove block from list of disabled blocks that have disabled use.

- **String blockName** block resource name

```
ConfigManager.removeDisabledBlockInStoneAge(String blockName);

ConfigManager.removeDisabledBlockInStoneAge("minecraft:dispenser");
```

## Addition

```zenscript
import mods.stone_age.ConfigManager;

ConfigManager.addDisabledBlockInStoneAge("minecraft:furnace", "minecraft:dispenser");

ConfigManager.removeDisabledBlockInStoneAge("minecraft:dispenser");

var blocks = ConfigManager.getDisabledBlocksInStoneAge();

for i in blocks {
	println(i as string);
}
```
