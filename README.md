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

Divided into 8 sub-mods, one mandatory (core) and 7 optional (loadable)

### Common

![common](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/89010ac6-9e0a-4354-8e7e-ea06a0590ba8)

Items:
* milk bowl, cheese, water bowl, salt
* dough
* ham, bacon, salami
* caramel
* strawberry, raspberry, cherry, orange, peach, pineapple, grape, vanilla, olives
* tomato, onion, potato (there was none so long ago), lettuce
* vegetable mix
* sinapis
* mustard, mayonnaise, ketchup

Code:
```
ModLoader.addShapelessRecipe(new ItemStack(bowlWater, 1), new Object [] {Item.bucketWater, Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlWater, 8), new Object [] {"###", "#%#", "###", Character.valueOf('%'), Item.bucketWater, Character.valueOf('#'), Item.bowlEmpty});
ModLoader.addSmelting(bowlWater.shiftedIndex, new ItemStack(salt, 1));
ModLoader.addShapelessRecipe(new ItemStack(bowlMilk, 1), new Object [] {Item.bucketMilk, Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMilk, 8), new Object [] {"###", "#%#", "###", Character.valueOf('%'), Item.bucketMilk, Character.valueOf('#'), Item.bowlEmpty});
ModLoader.addSmelting(bowlMilk.shiftedIndex, new ItemStack(cheese, 1));
ModLoader.addRecipe(new ItemStack(vegetables, 1), new Object [] {"ACD", "ABD", "BBD", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('C'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('D'), new ItemStack(Item.dyePowder, 1, 1)});
ModLoader.addRecipe(new ItemStack(tomato, 1), new Object [] {" % ", "###", " % ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(dough, 4), new Object [] {"ABA", "CDE", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(dough, 4), new Object [] {"ABA", "EDC", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(dough, 4), new Object [] {"ABA", "CDE", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(dough, 4), new Object [] {"ABA", "EDC", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(pineapple, 1), new Object [] {" % ", "#%#", " # ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(ham, 8), new Object [] {" #", "# ", Character.valueOf('#'), Item.porkCooked});
ModLoader.addRecipe(new ItemStack(salami, 12), new Object [] {" % ", "###", " % ", Character.valueOf('#'), Item.porkCooked, Character.valueOf('%'), Item.leather});
ModLoader.addRecipe(new ItemStack(olives, 1), new Object [] {" % ", "# #", " % ", Character.valueOf('#'), Block.vine, Character.valueOf('%'), new ItemStack(Item.dyePowder, 1, 0)});
ModLoader.addRecipe(new ItemStack(olives, 1), new Object [] {" # ", "% %", " # ", Character.valueOf('#'), Block.vine, Character.valueOf('%'), new ItemStack(Item.dyePowder, 1, 0)});
ModLoader.addSmelting(Item.ham.shiftedIndex, new ItemStack(Item.bacon, 1));
ModLoader.addRecipe(new ItemStack(lettuce, 1), new Object [] {" #%", "#%#", "%# ", Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 2)});
ModLoader.addRecipe(new ItemStack(lettuce, 1), new Object [] {"%# ", "#%#", " #%", Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 2)});
ModLoader.addRecipe(new ItemStack(ketchup, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.tomato, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(ketchup, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.tomato, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(ketchup, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.tomato, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(ketchup, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.tomato, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mayonnaise, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.egg, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mayonnaise, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.egg, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mayonnaise, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.egg, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mayonnaise, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.egg, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(onion, 1), new Object [] {" # ", "% %", " # ", Character.valueOf('%'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('#'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(onion, 1), new Object [] {" % ", "# #", " % ", Character.valueOf('%'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('#'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(potato, 1), new Object [] {" % ", "#$#", " % ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('$'), new ItemStack(Item.dyePowder, 1, 15)});
ModLoader.addRecipe(new ItemStack(potato, 1), new Object [] {" # ", "%$%", " # ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('$'), new ItemStack(Item.dyePowder, 1, 15)});
ModLoader.addRecipe(new ItemStack(sinapis, 1), new Object [] {" % ", "#$#", " % ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('$'), new ItemStack(Item.dyePowder, 1, 11)});
ModLoader.addRecipe(new ItemStack(sinapis, 1), new Object [] {" # ", "%$%", " # ", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('$'), new ItemStack(Item.dyePowder, 1, 11)});
ModLoader.addRecipe(new ItemStack(mustard, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.sinapis, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mustard, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bucketWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.sinapis, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mustard, 1), new Object [] {"BCD", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.sinapis, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(mustard, 1), new Object [] {"DCB", "AEA", " F ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.bowlWater, Character.valueOf('D'), Item.salt, Character.valueOf('E'), Item.sinapis, Character.valueOf('F'), Item.glassBottle});
ModLoader.addRecipe(new ItemStack(strawberry, 1), new Object [] {"BDB", "ACA", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('C'), Item.seeds, Character.valueOf('D'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(raspberry, 1), new Object [] {"DBD", "ACA", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('C'), Item.seeds, Character.valueOf('D'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(cherry, 1), new Object [] {"DBD", "ACA", "A A", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 1), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('C'), Item.seeds, Character.valueOf('D'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(orange, 1), new Object [] {"ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('B'), Item.appleRed});
ModLoader.addRecipe(new ItemStack(orange, 1), new Object [] {" A ", " B ", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('B'), Item.appleRed});
ModLoader.addRecipe(new ItemStack(peach, 1), new Object [] {"ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.appleRed});
ModLoader.addRecipe(new ItemStack(peach, 1), new Object [] {" A ", " B ", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 11), Character.valueOf('B'), Item.appleRed});
ModLoader.addRecipe(new ItemStack(grapes, 1), new Object [] {"ABA", "ACA", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 13), Character.valueOf('B'), Item.seeds, Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(grapes, 1), new Object [] {"ACA", "ABA", " A ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 13), Character.valueOf('B'), Item.seeds, Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(vanilla, 1), new Object [] {" AB", "ACA", "BA ", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addSmelting(Item.sugar.shiftedIndex, new ItemStack(Item.caramel, 1));
```

### Burgers

![burgers](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/83d56316-3b6f-4427-b66f-f62732910208)

Items:
* burger bun, beef patty, chicken patty, fish patty
* vegetable salad, Caesar salad
* ham burger, cheese burger, big burger, chicken burger, fish burger, bacon burger
* beef roll, chicken roll, fish roll
* french fries, chicken nuggets

Code:
```
ModLoader.addRecipe(new ItemStack(burgerBun, 1), new Object [] {"ABA", "CDE", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(burgerBun, 1), new Object [] {"ABA", "EDC", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(burgerBun, 1), new Object [] {"ABA", "CDE", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(burgerBun, 1), new Object [] {"ABA", "EDC", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(pattyBeef, 2), new Object [] {"#", "#", Character.valueOf('#'), Item.beefCooked});
ModLoader.addRecipe(new ItemStack(pattyChicken, 2), new Object [] {"#", "#", Character.valueOf('#'), Item.chickenCooked});
ModLoader.addRecipe(new ItemStack(pattyFish, 2), new Object [] {"#", "#", Character.valueOf('#'), Item.fishCooked});
ModLoader.addRecipe(new ItemStack(burgerHam, 1), new Object [] {"ABC", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.pattyBeef, Character.valueOf ('C'), Item.onion});
ModLoader.addRecipe(new ItemStack(burgerHam, 1), new Object [] {"CBA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.pattyBeef, Character.valueOf ('C'), Item.onion});
ModLoader.addRecipe(new ItemStack(burgerCheese, 1), new Object [] {"ABC", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.pattyBeef, Character.valueOf ('C'), Item.cheese});
ModLoader.addRecipe(new ItemStack(burgerCheese, 1), new Object [] {"CBA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.pattyBeef, Character.valueOf ('C'), Item.cheese});
ModLoader.addRecipe(new ItemStack(burgerBig, 1), new Object [] {"ABA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.cutletBeef, Character.valueOf ('B'), Item.lettuce});
ModLoader.addRecipe(new ItemStack(burgerChicken, 1), new Object [] {"ABC", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.mayonnaise, Character.valueOf ('B'), Item.pattyChicken, Character.valueOf ('C'), Item.lettuce});
ModLoader.addRecipe(new ItemStack(burgerChicken, 1), new Object [] {"CBA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.mayonnaise, Character.valueOf ('B'), Item.pattyChicken, Character.valueOf ('C'), Item.lettuce});
ModLoader.addRecipe(new ItemStack(burgerFish, 1), new Object [] {"ABC", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.mayonnaise, Character.valueOf ('B'), Item.pattyFish, Character.valueOf ('C'), Item.lettuce});
ModLoader.addRecipe(new ItemStack(burgerFish, 1), new Object [] {"CBA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.mayonnaise, Character.valueOf ('B'), Item.pattyFish, Character.valueOf ('C'), Item.lettuce});
ModLoader.addRecipe(new ItemStack(burgerBacon, 1), new Object [] {"ABC", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.bacon, Character.valueOf ('C'), Item.onion});
ModLoader.addRecipe(new ItemStack(burgerBacon, 1), new Object [] {"CBA", " # ", Character.valueOf('#'), Item.burgerBun, Character.valueOf ('A'), Item.ketchup, Character.valueOf ('B'), Item.bacon, Character.valueOf ('C'), Item.onion});
ModLoader.addRecipe(new ItemStack(rollBeef, 1), new Object [] {"ABA", "CDC", "ADA", Character.valueOf('A'), Item.dough, Character.valueOf ('B'), Item.pattyBeef, Character.valueOf ('C'), Item.lettuce, Character.valueOf ('D'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(rollChicken, 1), new Object [] {"ABA", "CDC", "ADA", Character.valueOf('A'), Item.dough, Character.valueOf ('B'), Item.pattyChicken, Character.valueOf ('C'), Item.lettuce, Character.valueOf ('D'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(rollFish, 1), new Object [] {"ABA", "CDC", "ADA", Character.valueOf('A'), Item.dough, Character.valueOf ('B'), Item.pattyFish, Character.valueOf ('C'), Item.lettuce, Character.valueOf ('D'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(chickenNuggets, 2), new Object [] {"%#%", Character.valueOf('#'), Item.chickenCooked, Character.valueOf('%'), Item.wheat});
ModLoader.addRecipe(new ItemStack(frenchFries, 1), new Object [] {"#", "%", "$", Character.valueOf('#'), Item.salt, Character.valueOf('%'), Item.potato, Character.valueOf('$'), Item.paper});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"AEB", "CFD", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"AEB", "DFC", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"BEA", "CFD", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"BEA", "DFC", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"CED", "AFB", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"CED", "BFA", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"DEC", "AFB", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlVegetableSalad, 1), new Object [] {"DEC", "BFA", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.olives, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"AEB", "CFD", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"AEB", "DFC", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"BEA", "CFD", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"BEA", "DFC", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"CED", "AFB", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"CED", "BFA", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"DEC", "AFB", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlCaesarSalad, 1), new Object [] {"DEC", "BFA", " G ", Character.valueOf('A'), Item.vegetables, Character.valueOf('B'), Item.lettuce, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.potato, Character.valueOf('E'), Item.chickenCooked, Character.valueOf('F'), Item.mayonnaise, Character.valueOf('G'), Item.bowlEmpty});
```

### Hotdogs

![hotdogs](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/f93227de-889f-48ad-8bef-9358638609e1)

Items:
* hotdog bun, pork sausage, beef sausage, chicken sausage
* standard hotdog, pork hotdog, beef hotdog, chicken hotdog, mild hotdog, spicy hotdog, cheese hotdog, bacon hotdog

Code:
```
ModLoader.addRecipe(new ItemStack(hotdogBun, 1), new Object [] {"CDE", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(hotdogBun, 1), new Object [] {"EDC", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(hotdogBun, 1), new Object [] {"CDE", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(hotdogBun, 1), new Object [] {"EDC", "ABA", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.salt});
ModLoader.addRecipe(new ItemStack(sausageBeef, 2), new Object [] {"##", Character.valueOf('#'), Item.beefCooked});
ModLoader.addRecipe(new ItemStack(sausageChicken, 2), new Object [] {"##", Character.valueOf('#'), Item.chickenCooked});
ModLoader.addRecipe(new ItemStack(sausagePork, 2), new Object [] {"##", Character.valueOf('#'), Item.porkCooked});
ModLoader.addRecipe(new ItemStack(hotdogStandard, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.vegetables, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogStandard, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.vegetables, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogMild, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.lettuce, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogMild, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.lettuce, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogSpicy, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausagePork, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.onion, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogSpicy, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausagePork, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.onion, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogBeef, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.lettuce, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogBeef, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.lettuce, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogPork, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausagePork, Character.valueOf('C'), Item.mayonnaise, Character.valueOf('D'), Item.vegetables, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogPork, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausagePork, Character.valueOf('C'), Item.mayonnaise, Character.valueOf('D'), Item.vegetables, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogChicken, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.onion, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogChicken, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.onion, Character.valueOf('E'), Item.mayonnaise});
ModLoader.addRecipe(new ItemStack(hotdogCheese, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.mayonnaise, Character.valueOf('D'), Item.cheese, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogCheese, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageBeef, Character.valueOf('C'), Item.mayonnaise, Character.valueOf('D'), Item.cheese, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogBacon, 1), new Object [] {"CDE", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.bacon, Character.valueOf('E'), Item.mustard});
ModLoader.addRecipe(new ItemStack(hotdogBacon, 1), new Object [] {"EDC", " B ", " A ", Character.valueOf('A'), Item.hotdogBun, Character.valueOf('B'), Item.sausageChicken, Character.valueOf('C'), Item.ketchup, Character.valueOf('D'), Item.bacon, Character.valueOf('E'), Item.mustard});
```

### Pizzas

![pizzas](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/30df576d-8b7d-40de-9cf9-de3bc48d5579)

Items:
* raw pizzas, raw slices, ready pizzas, ready slices: cheese, anchovy, vegetarian, ham, salami, mushroom, ham and mushroom, ham and pineapple, olive, artichoke, four season, assortie
* artichoke
* mushroom mix, ham mix, artichoke mix, olive mix, ham and mushroom mix, ham and pineapple mix, four seasons mix, assortie mix

Code:
```
ModLoader.addRecipe(new ItemStack(artichoke, 1), new Object [] {" A ", "BCB", " B ", Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 13), Character.valueOf('C'), Item.seeds});
ModLoader.addRecipe(new ItemStack(bowlMixMushrooms, 2), new Object [] {"AC", "BB", Character.valueOf('A'), BlockFlower.mushroomRed, Character.valueOf('C'), BlockFlower.mushroomBrown, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixMushrooms, 2), new Object [] {"CA", "BB", Character.valueOf('A'), BlockFlower.mushroomRed, Character.valueOf('C'), BlockFlower.mushroomBrown, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixHam, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.ham, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixArtichoke, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.artichoke, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixOlives, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.olives, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixHamMushrooms, 3), new Object [] {"ADC", "BBB", Character.valueOf('A'), BlockFlower.mushroomRed, Character.valueOf('C'), BlockFlower.mushroomBrown, Character.valueOf('B'), Item.bowlEmpty, Character.valueOf('D'), Item.ham});
ModLoader.addRecipe(new ItemStack(bowlMixHamMushrooms, 3), new Object [] {"CDA", "BBB", Character.valueOf('A'), BlockFlower.mushroomRed, Character.valueOf('C'), BlockFlower.mushroomBrown, Character.valueOf('B'), Item.bowlEmpty, Character.valueOf('D'), Item.ham});
ModLoader.addRecipe(new ItemStack(bowlMixHamPineapple, 3), new Object [] {"AC", "BB", Character.valueOf('A'), Item.ham, Character.valueOf('C'), Item.pineapple, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixHamPineapple, 3), new Object [] {"CA", "BB", Character.valueOf('A'), Item.ham, Character.valueOf('C'), Item.pineapple, Character.valueOf('B'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixSeasons, 8), new Object [] {"AAB", "D B", "DCC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BAB", "C C", "DAD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BAB", "D D", "CAC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CAC", "B B", "DAD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CAC", "D D", "BAB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DAD", "B B", "CAC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DAD", "C C", "BAB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ABA", "C C", "DBD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ABA", "D D", "CBC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CBC", "A A", "DBD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CBC", "D D", "ABA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DBD", "A A", "CBC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DBD", "C C", "ABA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ACA", "B B", "DCD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ACA", "D D", "BCB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BCB", "A A", "DCD", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BCB", "D D", "ACA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DCD", "A A", "BCB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"DCD", "B B", "ACA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ADA", "B B", "CDC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"ADA", "C C", "BDB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BDB", "A A", "CDC", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"BDB", "C C", "ADA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CDC", "A A", "BDB", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(bowlMixAssortie, 8), new Object [] {"CDC", "B B", "ADA", Character.valueOf('A'), Item.bowlMixHam, Character.valueOf('B'), Item.bowlMixOlives, Character.valueOf('C'), Item.bowlMixArtichoke, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawCheese, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.cheese});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawCheese, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.cheese});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawAnchovy, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.fishRaw});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawAnchovy, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.fishRaw});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawVegetarian, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.vegetables});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawVegetarian, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.vegetables});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHam, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.ham});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHam, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.ham});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawSalami, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.salami});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawSalami, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.salami});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawMush, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawMush, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixMushrooms});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHamNMush, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixHamMushrooms});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHamNMush, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixHamMushrooms});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHamNPine, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixHamPineapple});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawHamNPine, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixHamPineapple});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawOlives, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.olives});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawOlives, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.olives});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawartichoke, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.artichoke});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawartichoke, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.artichoke});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawSeasons, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixSeasons});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawSeasons, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixSeasons});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawAssortie, 1), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixAssortie});
ModLoader.addRecipe(new ItemStack(pizzaWholeRawAssortie, 1), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), Item.dough, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.tomato, Character.valueOf('D'), Item.bowlMixAssortie});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawCheese, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawCheese});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawAnchovy, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawAnchovy});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawVegetarian, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawVegetarian});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawHam, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawHam});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawSalami, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawSalami});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawMush, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawMush});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawHamNMush, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawHamNMush});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawHamNPine, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawHamNPine});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawOlives, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawOlives});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawartichoke, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawartichoke});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawSeasons, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawSeasons});
ModLoader.addRecipe(new ItemStack(pizzaSliceRawAssortie, 8), new Object [] {"#", Character.valueOf('#'), Item.pizzaWholeRawAssortie});
ModLoader.addSmelting(Item.pizzaWholeRawCheese.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedCheese, 1));
ModLoader.addSmelting(Item.pizzaWholeRawAnchovy.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedAnchovy, 1));
ModLoader.addSmelting(Item.pizzaWholeRawVegetarian.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedVegetarian, 1));
ModLoader.addSmelting(Item.pizzaWholeRawHam.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedHam, 1));
ModLoader.addSmelting(Item.pizzaWholeRawSalami.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedSalami, 1));
ModLoader.addSmelting(Item.pizzaWholeRawMush.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedMush, 1));
ModLoader.addSmelting(Item.pizzaWholeRawHamNMush.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedHamNMush, 1));
ModLoader.addSmelting(Item.pizzaWholeRawHamNPine.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedHamNPine, 1));
ModLoader.addSmelting(Item.pizzaWholeRawOlives.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedOlives, 1));
ModLoader.addSmelting(Item.pizzaWholeRawartichoke.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedartichoke, 1));
ModLoader.addSmelting(Item.pizzaWholeRawSeasons.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedSeasons, 1));
ModLoader.addSmelting(Item.pizzaWholeRawAssortie.shiftedIndex, new ItemStack(Item.pizzaWholeCoockedAssortie, 1));
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedCheese, 8), new Object [] {Item.pizzaWholeCoockedCheese});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedAnchovy, 8), new Object [] {Item.pizzaWholeCoockedAnchovy});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedVegetarian, 8), new Object [] {Item.pizzaWholeCoockedVegetarian});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedHam, 8), new Object [] {Item.pizzaWholeCoockedHam});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedSalami, 8), new Object [] {Item.pizzaWholeCoockedSalami});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedMush, 8), new Object [] {Item.pizzaWholeCoockedMush});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedHamNMush, 8), new Object [] {Item.pizzaWholeCoockedHamNMush});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedHamNPine, 8), new Object [] {Item.pizzaWholeCoockedHamNPine});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedOlives, 8), new Object [] {Item.pizzaWholeCoockedOlives});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedartichoke, 8), new Object [] {Item.pizzaWholeCoockedartichoke});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedSeasons, 8), new Object [] {Item.pizzaWholeCoockedSeasons});
ModLoader.addShapelessRecipe(new ItemStack(pizzaSliceCoockedAssortie, 8), new Object [] {Item.pizzaWholeCoockedAssortie});
ModLoader.addSmelting(Item.pizzaSliceRawCheese.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedCheese, 1));
ModLoader.addSmelting(Item.pizzaSliceRawAnchovy.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedAnchovy, 1));
ModLoader.addSmelting(Item.pizzaSliceRawVegetarian.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedVegetarian, 1));
ModLoader.addSmelting(Item.pizzaSliceRawHam.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedHam, 1));
ModLoader.addSmelting(Item.pizzaSliceRawSalami.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedSalami, 1));
ModLoader.addSmelting(Item.pizzaSliceRawMush.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedMush, 1));
ModLoader.addSmelting(Item.pizzaSliceRawHamNMush.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedHamNMush, 1));
ModLoader.addSmelting(Item.pizzaSliceRawHamNPine.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedHamNPine, 1));
ModLoader.addSmelting(Item.pizzaSliceRawOlives.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedOlives, 1));
ModLoader.addSmelting(Item.pizzaSliceRawartichoke.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedartichoke, 1));
ModLoader.addSmelting(Item.pizzaSliceRawSeasons.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedSeasons, 1));
ModLoader.addSmelting(Item.pizzaSliceRawAssortie.shiftedIndex, new ItemStack(Item.pizzaSliceCoockedAssortie, 1));
```

### Snacks

![snacks](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/2f1d284d-0053-45c2-87a1-b8ac779106ed)

Items:
* salt chips, cheese chips, onion chips, bacon chips
* flat choco bar, small choco bar, big choco bar
* baguette bun
* baguette with ham and cheese, baguette with salami, baguette with salami and cheese, baguette with salami and ham and cheese

Code:
```
ModLoader.addRecipe(new ItemStack(baguetteBun, 2), new Object [] {"CBA", "EAE", "ABD", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.salt, Character.valueOf('D'), Item.sugar, Character.valueOf('E'), Item.egg});
ModLoader.addRecipe(new ItemStack(baguetteBun, 2), new Object [] {"DBA", "EAE", "ABC", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bucketWater, Character.valueOf('C'), Item.salt, Character.valueOf('D'), Item.sugar, Character.valueOf('E'), Item.egg});
ModLoader.addRecipe(new ItemStack(baguetteBun, 2), new Object [] {"CBA", "EAE", "ABD", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.salt, Character.valueOf('D'), Item.sugar, Character.valueOf('E'), Item.egg});
ModLoader.addRecipe(new ItemStack(baguetteBun, 2), new Object [] {"DBA", "EAE", "ABC", Character.valueOf('A'), Item.wheat, Character.valueOf('B'), Item.bowlWater, Character.valueOf('C'), Item.salt, Character.valueOf('D'), Item.sugar, Character.valueOf('E'), Item.egg});
ModLoader.addRecipe(new ItemStack(baguetteHamCheese, 1), new Object [] {" A ", "BCB", " D ", Character.valueOf('A'), Item.mayonnaise, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.ham, Character.valueOf('D'), Item.baguetteBun});
ModLoader.addRecipe(new ItemStack(baguetteSalami, 1), new Object [] {"A", "C", "D", Character.valueOf('A'), Item.mayonnaise, Character.valueOf('C'), Item.ham, Character.valueOf('D'), Item.baguetteBun});
ModLoader.addRecipe(new ItemStack(baguetteSalamiCheese, 1), new Object [] {" A ", "BCB", " D ", Character.valueOf('A'), Item.mayonnaise, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.salami, Character.valueOf('D'), Item.baguetteBun});
ModLoader.addRecipe(new ItemStack(baguetteSalamiHamCheese, 1), new Object [] {"CAE", "B B", " D ", Character.valueOf('A'), Item.mayonnaise, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.ham, Character.valueOf('D'), Item.baguetteBun, Character.valueOf('E'), Item.salami});
ModLoader.addRecipe(new ItemStack(baguetteSalamiHamCheese, 1), new Object [] {"EAC", "B B", " D ", Character.valueOf('A'), Item.mayonnaise, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.ham, Character.valueOf('D'), Item.baguetteBun, Character.valueOf('E'), Item.salami});
ModLoader.addRecipe(new ItemStack(chipsSalt, 1), new Object [] {"A A", "DCD", " D ", Character.valueOf('A'), Item.salt, Character.valueOf('C'), Item.potato, Character.valueOf('D'), Item.paper});
ModLoader.addRecipe(new ItemStack(chipsCheese, 1), new Object [] {"ABA", "DCD", " D ", Character.valueOf('A'), Item.salt, Character.valueOf('B'), Item.cheese, Character.valueOf('C'), Item.potato, Character.valueOf('D'), Item.paper});
ModLoader.addRecipe(new ItemStack(chipsOnion, 1), new Object [] {"ABA", "DCD", " D ", Character.valueOf('A'), Item.salt, Character.valueOf('B'), Item.onion, Character.valueOf('C'), Item.potato, Character.valueOf('D'), Item.paper});
ModLoader.addRecipe(new ItemStack(chipsBacon, 1), new Object [] {"ABA", "DCD", " D ", Character.valueOf('A'), Item.salt, Character.valueOf('B'), Item.bacon, Character.valueOf('C'), Item.potato, Character.valueOf('D'), Item.paper});
ModLoader.addRecipe(new ItemStack(chocoBarFlat, 4), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bucketMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.salt});
ModLoader.addRecipe(new ItemStack(chocoBarFlat, 4), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bucketMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.salt});
ModLoader.addRecipe(new ItemStack(chocoBarFlat, 4), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bowlMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.salt});
ModLoader.addRecipe(new ItemStack(chocoBarFlat, 4), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bowlMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.salt});
ModLoader.addRecipe(new ItemStack(chocoBarBig, 2), new Object [] {"AEA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bucketMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.caramel});
ModLoader.addRecipe(new ItemStack(chocoBarBig, 2), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bucketMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.caramel});
ModLoader.addRecipe(new ItemStack(chocoBarBig, 2), new Object [] {"AEA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bowlMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.caramel});
ModLoader.addRecipe(new ItemStack(chocoBarBig, 2), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bowlMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.caramel});
ModLoader.addRecipe(new ItemStack(chocoBarSmall, 2), new Object [] {"AEA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bucketMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.sugar});
ModLoader.addRecipe(new ItemStack(chocoBarSmall, 2), new Object [] {"AEA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.bowlMilk, Character.valueOf('C'), Item.sugar, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.sugar});
```

### Sushi

![sushi](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/120338dd-d24f-44c1-838c-da0eb14bcd25)

Items:
* rice, nori, caviar (roe), wasabi
* nigirisushi, gunkanmaki, futomaki, hosomaki, uramaki, inarisushi

Code:
```
ModLoader.addRecipe(new ItemStack(rice, 1), new Object [] {"ABA", "BCB", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('C'), Item.bucketWater});
ModLoader.addRecipe(new ItemStack(rice, 1), new Object [] {"BAB", "ACA", "BAB", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('C'), Item.bucketWater});
ModLoader.addRecipe(new ItemStack(rice, 1), new Object [] {"ABA", "BCB", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('C'), Item.bowlWater});
ModLoader.addRecipe(new ItemStack(rice, 1), new Object [] {"BAB", "ACA", "BAB", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 15), Character.valueOf('B'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('C'), Item.bowlWater});
ModLoader.addRecipe(new ItemStack(nori, 4), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('D'), Item.bucketWater});
ModLoader.addRecipe(new ItemStack(nori, 4), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('D'), Item.bucketWater});
ModLoader.addRecipe(new ItemStack(nori, 4), new Object [] {"ABA", "CDC", "ABA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('D'), Item.bowlWater});
ModLoader.addRecipe(new ItemStack(nori, 4), new Object [] {"ACA", "BDB", "ACA", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 2), Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 0), Character.valueOf('C'), new ItemStack(BlockTallGrass.tallGrass, 1, 1), Character.valueOf('D'), Item.bowlWater});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"A", "B", "C", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"A", "C", "B", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"B", "A", "C", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"B", "C", "A", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"C", "A", "B", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(caviar, 1), new Object [] {"C", "B", "A", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), new ItemStack(Item.dyePowder, 1, 14), Character.valueOf('C'), Item.egg});
ModLoader.addRecipe(new ItemStack(wasabi, 1), new Object [] {"#", "%", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 10), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(wasabi, 1), new Object [] {"%", "#", Character.valueOf('#'), new ItemStack(Item.dyePowder, 1, 10), Character.valueOf('%'), new ItemStack(BlockTallGrass.tallGrass, 1, 1)});
ModLoader.addRecipe(new ItemStack(sushiNigirizushi, 2), new Object [] {"A", "B", "C", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), Item.nori, Character.valueOf('C'), Item.rice});
ModLoader.addRecipe(new ItemStack(sushiGunkanmaki, 4), new Object [] {"AA", "BC", "CB", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.nori, Character.valueOf('C'), Item.rice});
ModLoader.addRecipe(new ItemStack(sushiGunkanmaki, 4), new Object [] {"AA", "CB", "BC", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.nori, Character.valueOf('C'), Item.rice});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"ABC", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"ACB", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"BAC", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"BCA", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"CAB", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiFutomaki, 2), new Object [] {"CBA", " D ", " E ", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.fishRaw, Character.valueOf('C'), Item.wasabi, Character.valueOf('D'), Item.rice, Character.valueOf('E'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiHosomaki, 4), new Object [] {"A", "B", "C", Character.valueOf('A'), Item.fishRaw, Character.valueOf('B'), Item.rice, Character.valueOf('C'), Item.nori});
ModLoader.addRecipe(new ItemStack(sushiUramaki, 6), new Object [] {"ABA", "CDC", Character.valueOf('A'), Item.caviar, Character.valueOf('B'), Item.wasabi, Character.valueOf('C'), Item.nori, Character.valueOf('D'), Item.rice});
ModLoader.addRecipe(new ItemStack(sushiInarizushi, 1), new Object [] {"ABA", Character.valueOf('A'), Item.rice, Character.valueOf('B'), Item.wasabi});
```

### Ice cream

![icecreams](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/79359d73-3470-4461-9b12-2587f5d5a864)

Items:
* ice balls, paper cups, waffle cups, waffle cones: apple, choco, melon, pineapple, strawberry, raspberry, cherry, orange, peach, grape, vanilla, caramel, stracciatella (vanilla with choco chips or crumbs)
* vanilla and chocolate mix
* paper cup, waffle cup, waffle cone

Code:
```
ModLoader.addRecipe(new ItemStack(bowlMixStracciatella, 1), new Object [] {"A", "B", "C", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.vanilla, Character.valueOf('C'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(bowlMixStracciatella, 1), new Object [] {"B", "A", "C", Character.valueOf('A'), new ItemStack(Item.dyePowder, 1, 3), Character.valueOf('B'), Item.vanilla, Character.valueOf('C'), Item.bowlEmpty});
ModLoader.addRecipe(new ItemStack(icePaperCup, 3), new Object [] {"% %", "%%%", Character.valueOf('%'), Item.paper});
ModLoader.addRecipe(new ItemStack(iceWaffleCup, 3), new Object [] {"% %", "%%%", Character.valueOf('%'), Item.dough});
ModLoader.addRecipe(new ItemStack(iceWaffleCone, 2), new Object [] {"% %", "% %", " % ", Character.valueOf('%'), Item.dough});
ModLoader.addRecipe(new ItemStack(iceBallApple, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.appleRed});
ModLoader.addRecipe(new ItemStack(iceBallChoco, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), new ItemStack(Item.dyePowder, 1, 3)});
ModLoader.addRecipe(new ItemStack(iceBallMelon, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.melon});
ModLoader.addRecipe(new ItemStack(iceBallPineapple, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.pineapple});
ModLoader.addRecipe(new ItemStack(iceBallStrawberry, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.strawberry});
ModLoader.addRecipe(new ItemStack(iceBallRaspberry, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.raspberry});
ModLoader.addRecipe(new ItemStack(iceBallCherry, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.cherry});
ModLoader.addRecipe(new ItemStack(iceBallOrange, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.orange});
ModLoader.addRecipe(new ItemStack(iceBallPeach, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.peach});
ModLoader.addRecipe(new ItemStack(iceBallGrape, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.grapes});
ModLoader.addRecipe(new ItemStack(iceBallVanilla, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.vanilla});
ModLoader.addRecipe(new ItemStack(iceBallCaramel, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.caramel});
ModLoader.addRecipe(new ItemStack(iceBallStracciatella, 1), new Object [] {"ABA", "CDC", "AEA", Character.valueOf('A'), Item.bucketMilk, Character.valueOf('B'), Item.sugar, Character.valueOf('C'), Item.snowball, Character.valueOf('D'), Item.egg, Character.valueOf('E'), Item.bowlMixStracciatella});
ModLoader.addRecipe(new ItemStack(icePaperCupApple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallApple, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupChoco, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallChoco, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupMelon, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallMelon, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupPineapple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPineapple, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupStrawberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStrawberry, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupRaspberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallRaspberry, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupCherry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCherry, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupOrange, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallOrange, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupPeach, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPeach, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupGrape, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallGrape, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupVanilla, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallVanilla, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupCaramel, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCaramel, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(icePaperCupStracciatella, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStracciatella, Character.valueOf('B'), Item.icePaperCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupApple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallApple, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupChoco, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallChoco, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupMelon, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallMelon, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupPineapple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPineapple, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupStrawberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStrawberry, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupRaspberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallRaspberry, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupCherry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCherry, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupOrange, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallOrange, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupPeach, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPeach, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupGrape, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallGrape, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupVanilla, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallVanilla, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupCaramel, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCaramel, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleCupStracciatella, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStracciatella, Character.valueOf('B'), Item.iceWaffleCup});
ModLoader.addRecipe(new ItemStack(iceWaffleConeApple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallApple, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeChoco, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallChoco, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeMelon, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallMelon, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConePineapple, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPineapple, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeStrawberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStrawberry, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeRaspberry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallRaspberry, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeCherry, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCherry, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeOrange, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallOrange, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConePeach, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallPeach, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeGrape, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallGrape, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeVanilla, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallVanilla, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeCaramel, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallCaramel, Character.valueOf('B'), Item.iceWaffleCone});
ModLoader.addRecipe(new ItemStack(iceWaffleConeStracciatella, 1), new Object [] {"A", "B", Character.valueOf('A'), Item.iceBallStracciatella, Character.valueOf('B'), Item.iceWaffleCone});
```

### Drinks

![drinks](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/16600de0-950b-4236-ac19-bb8df9a4fc8c)

Items:
* juices: apple, tomato, pineapple, cherry, orange, peach, grape, berry, multifruit
* berry mix, multifruit mix
* milk shakes: apple, choco, strawberry, raspberry, cherry, vanilla, caramel
* ice teas: strawberry, orange, peach
* fizzy drinks: cola, orange (Fanta reference), lime (Sprite reference)
* chicory, coffee, grass tea
