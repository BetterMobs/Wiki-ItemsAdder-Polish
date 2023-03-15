# DecentHolograms

## [Download here](https://www.spigotmc.org/resources/96927/)

## Jak wyświetlić niestandardowy przedmiot?

- Uruchom `/iacustommodeldata <item>` (np. `/iacustommodeldata ruby`)
- Zapamiętaj bazowy element i `CustomModelData` używane przez customowy element (np. `IRON_INGOT` i `10000`)
- Utwórz nowy hologram używając `/dh create <name> [Line]` (Możesz to pominąć, jeśli masz już hologram).
- Dodaj element do hologramu używając `/dh l add <name> <page> #ICON: <item> {CustomModelData: <cmd>}` (czyli np. `/dh l add example 1 #ICON: IRON_INGOT {CustomModelData: 10000}`)

{% hint style="success" %}
Czy podczas tworzenia hologramu można podać `#ICON: <item> {CustomModelData: <cmd>}` jako pierwszą linię w `/dh create`.  
Przykład: `/dh create example #ICON: IRON_INGOT {CustomModelData: 10000}`
{% endhint %}
