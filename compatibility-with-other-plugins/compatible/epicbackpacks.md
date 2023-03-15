# EpicBackpacks

## [Pobierz plugin plecaka tutaj](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-epic-backpacks.28981/)

{% hint style="warning" %}
Musisz mieć zainstalowany [DefaultPack](../../first-install.md#default-pack-optional)!
{% endhint %}

{% hint style="success" %}
Aby stworzyć plecaki, które będą korzystać z tekstury ItemsAdder musisz otworzyć backpacks.yml (w folderze EpicBackpacks) i dodać to (po jednym dla każdego plecaka, który chcesz stworzyć):
{% endhint %}

```yaml
 cool_backpack:
    display_name: '&fCool Backpack'
    item:
      type: ITEMSADDER_ITEM
      name: "iageneric:plastic_bag"
    size: 3
    craft_recipe:
      pattern:
        - XXX
        - LCL
        - XLX
      ingredients:
        L: LEATHER
        C: CHEST
```
