# ⚠ Nie kompatybilne

_**Czy jest to kompatybilne za pluginem X?**_

Nie mogę z pewnością odpowiedzieć na to pytanie, ponieważ nie mogę wiedzieć, jak każda wtyczka na świecie jest zakodowana, ale oto lista wtyczek, które mogą powodować problemy:

* Wszystkie pluginy, które używają **customową paczkę zasobów** (możesz sprawić, że będą kompatybilne, jeśli masz minimalną wiedzę na temat ręcznego łączenia resourcepacków, upewnij się, że nie zastąpisz plików ItemsAdder i gotowe)
* [CraftEnhance](https://www.spigotmc.org/resources/custom-recipes-and-crafting-craftenhance.65058/), ta wtyczka psuje logikę niestandardowych receptur ItemsAdder i tworzy błędy duplikacji. Więc proszę nie używać go
* Pluginy, które dostosowują zachowanie stołu do craftingu i receptur
* [LootChest ](https://www.spigotmc.org/resources/lootchest.61564/)może stwarzać kilka problemów [problemy](https://github.com/LoneDev6/ItemsAdder/issues/15#issuecomment-512990849)
* Na razie nie jest to **kompatybilne** z **pluginami** i generatorami świata, które **wyrzucają grzybki** z różnymi twarzami, aby stworzyć niestandardowe tekstury. W przyszłości dodam kompatybilność.
