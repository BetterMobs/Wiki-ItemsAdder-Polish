# Holographic Displays

# Jak korzystać w emoji w hologramach

* Pobierz [Holographic Displays](https://dev.bukkit.org/projects/holographic-displays)
* Pobierz [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)
* Pobierz [HolographicExtension addon](https://www.spigotmc.org/resources/holographicextension.18461/)

Teraz możesz używać [fontów ](../../plugin-usage/adding-content/font-images/)(**emojis**) wewnątrz tekstów hologramów i wszędzie we wszystkich wtyczkach, które wspierają **PlaceholderAPI**, w tym przypadku **Holographic Displays**.
Oto kod: `%img_NAME%` zamiast NAME wpisz nazwę fontu, który ma być obrazem.
Na przykład: `%img_smile%`.

Aby stworzyć hologram możesz użyć np. tych poleceń:

`/holo create test_itemsadder Hello! %img_smile%`

![](<../../.gitbook/assets/image (20).png>)

## Jak dodać pływający element niestandardowy?

* uruchom `/iacustommodeldata <item>` (na przykład `/iacustommodeldata ruby`)
* skopiuj `CustomModelData`, na przykład `10000`
* utwórz nowy hologram, na przykład: `/hd create holo_icon Hello!`.
* dodaj pływający element do hologramu, określając **typ holo** i **CustomModelData**. Przykład: `/hd addline holo_icon ICON: IRON_INGOT {CustomModelData: 10000}`

![](<../../.gitbook/assets/image_(124).png>)



``
