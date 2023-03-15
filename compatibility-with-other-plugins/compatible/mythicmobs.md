# Mythicmobs

### [Pobierz tutaj](https://www.spigotmc.org/resources/%E2%9A%94-mythicmobs-free-version-%E2%96%BAthe-1-custom-mob-creator%E2%97%84.5702/)

## Używanie elementów ItemsAdder w MythicMobs&#x20;

{% hint style="warning" %}
Zaktualizuj do wersji **ItemsAdder 3.0.4** lub wyższej i **MythicMobs 5.0.1** lub wyższej.
{endhint %}

### Spadki

Przykład: drop niestandardowego przedmiotu o 30% szansie i ilości od 1 do 5.

```yaml
ninja_skeleton:
  Typ: ZOMBIE
  Wyświetlacz: '&aNinja Skeleton'
  Zdrowie: 10
  Obrażenia: 2
  Dropsy:
    - myitems:special_sword 1-5 30%
  Opcje:
    MovementSpeed: 0
    Silent: true
  Umiejętności:
  - customentity{model=custom:ninja_skeleton} @self ~onSpawn
  - customentity{play=attack} @self ~onAttack
  - customentity{walk=b_walk} @self ~onAttack
```

### Sprzęt

```yaml
SkeletalKnight:
  Typ: WITHER_SKELETON
  Wyświetleń: '&aSkeletal Knight'
  Zdrowie: 40
  Obrażenia: 8
  Wyposażenie:
  - myitems:special_hełm HEŁM
  - myitems:special_chestplate CHEST
  - myitems:special_legginsy NOGI
  - mojeitems:special_boots FEET
  - przedmioty:specjalne_miecz DŁOŃ
  - mojaitems:special_shield OFFHAND
```

## Custom mobs models

{% content-ref url="../../plugin-usage/adding-content/mobs/advanced-method/" %}
[advanced-method](../../plugin-usage/adding-content/mobs/advanced-method/)
{% endcontent-ref %}
