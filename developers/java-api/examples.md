# Użycie

## Pobranie API

{% embed url="https://github.com/LoneDev6/API-ItemsAdder" %}

## Przedmioty niestandardowe - [docs](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomStack.java)

#### Pobieranie niestandardowego elementu dowolnego typu (blok, przedmiot, kapelusz, jedzenie itp.) według id lub namespace:id

```java
CustomStack stack = CustomStack.getInstance("your_item")
if(stack != null)
{
    ItemStack itemStack = stack.getItemStack();
}
else
{
    //nie znaleziono elementu niestandardowego o tym id
}
```

#### Sprawdzanie, czy dany element istnieje

```java
CustomStack.isInRegistry("your_item")
```

#### Uzyskanie CustomStack z Bukkit ItemStack

```java
CustomStack stack = CustomStack.byItemStack(myItemStack);

if(stack != null) // To niestandardowy element!
{
    stack.setUsages(5) // Dla przykładu ustawiamy "usage
    // ...
}
else // To nie jest element niestandardowy!
{
     // ...
}
```

## Custom Blocks - [docs](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomBlock.java)

#### Sprawdź czy istnieje własny blok

```java
CustomBlock.isInRegistry("your_item")
```

#### Sprawdź czy blok światowy jest blokiem niestandardowym

```java
CustomBlock customBlock = CustomBlock.byAlreadyPlaced(block);
if(customBlock != null)
{
    // Blok niestandardowy, zrób tutaj swoje własne rzeczy
}
else
{
    // Nie jest to blok własny
}
```

#### Umieść własny blok

```java
CustomBlock customBlock = CustomBlock.getInstance("ruby_ore");
if(customBlock != null) //niezbędne, jeśli jesteś pewien, że bloki istnieją.
{
    customBlock.place(location);
}
else
{
    // Niestandardowy blok nie został znaleziony w konfiguracjach ItemsAdder!
}
```

## Custom entity - [docs](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomEntity.java)

#### Spawn a custom mob by id or namespace:id

```java
CustomEntity customEntity = CustomEntity.spawn("your_item", location)
if(customEntity != null)
{
    // Pomiot niestandardowy
    
    // Przykład: drukuj w konsoli identyfikator z nazwą
    System.out.println(customEntity.getNamespacedID())
}
else
{
    // Niestandardowa encja nie została znaleziona w konfiguracjach ItemsAdder!
}
```

### Uzyskanie niestandardowej encji przez już spłodzoną encję Bukkit

```java
CustomEntity customEntity = CustomEntity.byAlreadySpawned(entity)
if(customEntity != null)
{
    // To jest niestandardowa encja
    
    // Przykład: wypisanie w konsoli nazwy podmiotu
    System.out.println(customEntity.getNamespacedID())
}
else
{
    // Ta encja Bukkit nie jest encją niestandardową!
}
```

## API płynów

Proszę również zainstalować addon [IALiquids ](https://www.spigotmc.org/resources/84386)aby mieć kilka testowych płynów.

```java
@EventHandler
void interact(PlayerInteractEvent e)
{
    if(e.getAction() == Action.LEFT_CLICK_BLOCK)
    {
        ItemsAdder.setLiquid("ialiquids:red_water", e.getClickedBlock().getLocation());
    }
    else if(e.getAction() == Action.RIGHT_CLICK_BLOCK)
    {
        System.out.println(ItemsAdder.getLiquidName(e.getClickedBlock().getRelative(e.getBlockFace()).getLocation()));
