# ExcellentEnchants

[Pobierz tutaj](https://www.spigotmc.org/resources/goldenenchants-%E2%80%A2-more-vanilla-like-enchantments-1-14-1-16.61693/)

(wcześniej znany jako **GoldenEnchants**)

## Jak używać enchantów

To jest przykładowa konfiguracja dla ItemsAdder custom item enchant.

{% hint style="warning" %}
Ostrzeżenie: enchanty nie będą wyświetlane w lore przedmiotu, jest to "bug" innego pluginu.

<mark style="color:green;">Efekt nadal będzie działał!</mark>.

Więc powinieneś napisać lore na własną rękę.
{% endhint %}

```yaml
  ruby_pickaxe:
    display_name: display-name-ruby_pickaxe
    permission: ruby_pickaxe
    resource:
      material: DIAMOND_PICKAXE
      generate: true
      textures:
      - item/ruby_pickaxe.png
    enchants:
    - tunnel:1
```

In this case I set `tunnel` enchant with level 1

