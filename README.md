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

### Burgers

![burgers](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/83d56316-3b6f-4427-b66f-f62732910208)

Items:
* burger bun, beef patty, chicken patty, fish patty
* vegetable salad, Caesar salad
* ham burger, cheese burger, big burger, chicken burger, fish burger, bacon burger
* beef roll, chicken roll, fish roll
* french fries, chicken nuggets

### Hotdogs

![hotdogs](https://github.com/MxGrv/Minecraft-Ideas/assets/18613763/f93227de-889f-48ad-8bef-9358638609e1)

Items:
* hotdog bun, pork sausage, beef sausage, chicken sausage
* standard hotdog, pork hotdog, beef hotdog, chicken hotdog, mild hotdog, spicy hotdog, cheese hotdog, bacon hotdog

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
