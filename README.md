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

### Snacks

![snacks](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/2f1d284d-0053-45c2-87a1-b8ac779106ed)

Items:
* salt chips, cheese chips, onion chips, bacon chips
* flat choco bar, small choco bar, big choco bar
* baguette bun
* baguette with ham and cheese, baguette with salami, baguette with salami and cheese, baguette with salami and ham and cheese

### Sushi

![sushi](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/120338dd-d24f-44c1-838c-da0eb14bcd25)

Items:
* rice, nori, caviar, wasabi
* nigirisushi, gunkanmaki, futomaki, hosomaki, uramaki, inarisushi

### Ice cream

![icecreams](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/79359d73-3470-4461-9b12-2587f5d5a864)

Items:
* ice balls, paper cups, waffle cups, waffle cones: apple, choco, melon, pineapple, strawberry, raspberry, cherry, orange, peach, grape, vanilla, caramel, stracciatella (vanilla with choco chips or crumbs)
* vanilla and chocolate mix
* paper cup, waffle cup, waffle cone

### Drinks

![drinks](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/16600de0-950b-4236-ac19-bb8df9a4fc8c)

Items:
* juices: apple, tomato, pineapple, cherry, orange, peach, grape, berry, multifruit
* berry mix, multifruit mix
* milk shakes: apple, choco, strawberry, raspberry, cherry, vanilla, caramel
* ice teas: strawberry, orange, peach
* fizzy drinks: cola, orange (Fanta reference), lime (Sprite reference)
* chicory, coffee, grass tea
