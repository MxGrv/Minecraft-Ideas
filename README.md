# Minecraft-Ideas
Ideas for Minecraft mods, ever visited me, since the far 1.8 Beta, some code and pictures
Note that many years have passed since then, but still I decided to share some unaccomplished work, because of the wasted time regrets, but I hope someone would find it all useful someday :)

## Medieval mod

### Common: blocks, items, food, weapons

![common](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/87506e24-3a6b-405d-b61d-28237c9763fa)

Several more melee weapons - spear, battle axe, halberdier, mace, dagger - all made of wood, stone, iron, gold and diamonds
Crossbow and bolts for it; whole copy of a bow
Throwable stone - thanks Stronghold 2 game for the idea; whole copy of a snowball
Salt, water bowl, millet gruel (porridge) bowl
Some goblets (chalices, cups), made of clay - crude (raw, unfired, unbaked - needs to be burned in a furnace), empty, with apple juice, with bear, with wine
While cobblestone, stone and stone bricks, as an opposition to the usual grey ones

Some notable crafting code:
```
ModLoader.addRecipe(new ItemStack(spearWood, 1), new Object [] {"  #", " % ", "%  ", Character.valueOf('#'), Block.planks, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(spearWood, 1), new Object [] {"#  ", " % ", "  %", Character.valueOf('#'), Block.planks, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(battleaxeStone, 1), new Object [] {"#%#", "#%#", " % ", Character.valueOf('#'), Block.cobblestone, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(halberdierIron, 1), new Object [] {"###", "#% ", " % ", Character.valueOf('#'), Item.ingotIron, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(halberdierIron, 1), new Object [] {"###", " %#", " % ", Character.valueOf('#'), Item.ingotIron, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(maceGold, 1), new Object [] {" # ", "#%#", " % ", Character.valueOf('#'), Item.ingotGold, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(daggerDiamond, 1), new Object [] {" #", "% ", Character.valueOf('#'), Item.diamond, Character.valueOf('%'), Item.stick});
ModLoader.addRecipe(new ItemStack(daggerDiamond, 1), new Object [] {"# ", " %", Character.valueOf('#'), Item.diamond, Character.valueOf('%'), Item.stick});

ModLoader.addRecipe(new ItemStack(crossbow, 1), new Object[] {"ABC", "BDA", "CAD", Character.valueOf('A'), Block.planks, Character.valueOf('B'), Item.silk, Character.valueOf('C'), Item.stick, Character.valueOf('D'), Item.ingotIron});
ModLoader.addRecipe(new ItemStack(crossbow, 1), new Object[] {"CBA", "ADB", "DAC", Character.valueOf('A'), Block.planks, Character.valueOf('B'), Item.silk, Character.valueOf('C'), Item.stick, Character.valueOf('D'), Item.ingotIron});
ModLoader.addRecipe(new ItemStack(bolt, 4), new Object [] {"A", "B", "C", Character.valueOf('A'), Item.ingotIron, Character.valueOf('B'), Item.stick, Character.valueOf('C'), Item.feather});
ModLoader.addRecipe(new ItemStack(throwingStone, 16), new Object [] {" # ", "# #", " # ", Character.valueOf('#'), Block.cobblestone});

ModLoader.addSmelting(bowlWater.shiftedIndex, new ItemStack(salt, 1)); 
ModLoader.addRecipe(new ItemStack(bowlWater, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.bucketWater, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlPorridge, 1), new Object [] {"BAB", "CDC", " E ", Character.valueOf('A'), Item.bucketWater, Character.valueOf('B'), Item.wheat, Character.valueOf('C'), Item.bucketMilk, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.bowlEmpty});

ModLoader.addRecipe(new ItemStack(gobletCrude, 1), new Object [] {"A A", " B ", "ABA", Character.valueOf('A'), Item.clay, Character.valueOf('B'), Item.stick});
ModLoader.addSmelting(gobletCrude.shiftedIndex, new ItemStack(gobletEmpty, 1));
ModLoader.addRecipe(new ItemStack(gobletJuice, 1), new Object [] {" A ", "BCB", " D ", Character.valueOf('A'), Item.bucketWater, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('C'), Item.appleRed, Character.valueOf('D'), mod_Medieval.gobletEmpty});
ModLoader.addRecipe(new ItemStack(gobletBeer, 1), new Object [] {" A ", "BCB", " D ", Character.valueOf('A'), Item.bucketWater, Character.valueOf('B'), Item.seeds, Character.valueOf('C'), Item.wheat, Character.valueOf('D'), mod_Medieval.gobletEmpty});
ModLoader.addRecipe(new ItemStack(gobletWine, 1), new Object [] {" A ", "BCB", " D ", Character.valueOf('A'), Item.bucketWater, Character.valueOf('B'), Block.vine, Character.valueOf('C'), new ItemStack(Item.dyePowder, 1, 13), Character.valueOf('D'), mod_Medieval.gobletEmpty});
```

### Coats (crests)

![coats](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/53e2b8de-c3b4-4730-943b-f3b8cc54b80c)

Coats of arms, crests, personal logos, all in white-black to provide authentic coloring later - once again, thanks Stronghold 2 game for the idea
The figures are:
* squares, english cross, diagonal line, chevron, scottish cross
* lion, dragon or wyvern, unicorn, griffin, (german) eagle, chimaera, dog (wolf) head, snake
* skull, goblet (chalice, cup), french royal lily (fleur-de-lis), tower, wall
* polar star, snowflake, sun

### Also

Clay biome to provide enough red bricks
Blocks:
* roof tile - out of clay
* wattle - basically a fence, but in the other design
* wheat haystack
Items:
* acorns - dropped from oaks
* corned goods - chicken, beef, pork, fish - crafted with salt

Some notable crafting code:
```
ModLoader.addRecipe(new ItemStack(roofTile, 2), new Object [] {"#%#", "A%A", "#%#", Character.valueOf('#'), Item.brick, Character.valueOf('%'), Item.stick, Character.valueOf('A'), Item.silk});
ModLoader.addRecipe(new ItemStack(wattle, 3), new Object [] {"#X#", "XZX", "#X#", Character.valueOf('#'), Block.planks, Character.valueOf('X'), Item.stick, Character.valueOf('Z'), Item.silk});
ModLoader.addRecipe(new ItemStack(haystack, 1), new Object [] {"###", "%%%", "###", Character.valueOf('#'), Item.wheat, Character.valueOf('%'), Item.silk});
```

## Fast Food mod
