# Narzędzia API

## Narzędzia API

To są niektóre statyczne narzędzia do szybkiego uzyskania pewnych informacji.

{% hint style="warning" %}
Zauważ, że te statyczne metody narzędziowe są przeznaczone do leniwego użycia, powinieneś użyć innych klas API zamiast tego.
{endhint %}

```java
// Sprawdza czy itemsadder zakończył ładowanie swoich elementów i czy są one dostępne
// Normalnie powinieneś użyć ItemsAdderFirstLoadEvent zamiast tego.
// ale czasami możesz potrzebować sprawdzić to również programowo.
public static boolean areItemsLoaded()

/Sprawdza, czy element jest elementem niestandardowym wykonanym za pomocą ItemsAdder.
public static boolean isCustomItem(ItemStack itemStack)
public static boolean isCustomItem(String customItemName)

//zwraca ItemStack niestandardowego bloku w świecie
public static ItemStack getCustomBlock(Block block)

//sprawdza, czy obiekt w świecie jest meblem
public static boolean isFurniture(Entity entity)

//sprawdzenie, czy ItemStack jest określonym elementem niestandardowym 
//(przykład: sprawdzenie czy kilof jest 'amethyst_pickaxe')
public static boolean matchCustomItemName(ItemStack itemStack, String customItemName)
```

## Stare metody API.

{% hint style="warning" %}
To jest stare API, nadal jest dostępne i działa dobrze.
{endhint %}

```java
//Uzyskanie elementu niestandardowego ItemsAdder według jego nazwy w konfiguracji
public static ItemStack getCustomItem(String nameInConfig)

//Spawns blok wykonany z ItemsAdder określający itemstack 
//(uzyskać go przy pomocy getCustomItem)
public static void placeCustomBlock(Location location, ItemStack customBlock)
public static void placeCustomBlock(Location location, ItemStack customBlock, boolean lightweight)

//zbierz łupy z bloku niestandardowego
public static List<ItemStack> getCustomBlockLoot(Block block, ItemStack tool, boolean includeSelfBlock)

/Sprawdzanie czy blok na świecie jest blokiem niestandardowym wykonanym za pomocą ItemsAdder
public static boolean isCustomBlock(Block block)

//rozmieszcza niestandardowe nasiona tak, jak zrobiłby to normalny gracz
public static void placeCustomCrop(Location location, ItemStack seed)

//sprawdza czy blok jest niestandardową rośliną z niestandardowymi nasionami
public static boolean isCustomCrop(Block block)

//zapoznaj się z niestandardowym ziarnem niestandardowej uprawy
public static String getCustomSeedNameFromCrop(Block block)

//zapoznaj się z nazwą elementu w configu (np. 'ruby_pickaxe')
public static String getCustomItemName(ItemStack itemStack)

//zapozna się z nazwą konfiguracji, w której dany element jest zadeklarowany (np. 'items/swords')
public static String getCustomItemFileName(ItemStack itemStack)

//zapyta o pozostałą ilość zastosowań tego elementu (-999 jeżeli nie ma określonych zastosowań = infinite)
public static int getCustomItemUsages(ItemStack itemStack)

//ustala niestandardową trwałość przedmiotu (działa również z przedmiotami waniliowymi i z
//niestandardowymi przedmiotami z domyślną trwałością waniliową)
public static ItemStack setCustomItemDurability(ItemStack item, int durability)

//uzyskaj niestandardową trwałość
public static int getCustomItemDurability(ItemStack itemStack)

//zapoznaj się z maksymalną niestandardową trwałością 
public static int getCustomItemMaxDurability(ItemStack itemStack)
```
