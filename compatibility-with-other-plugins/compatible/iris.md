# Iris

## [Pobierz tutaj](https://www.spigotmc.org/resources/iris-world-gen-custom-biome-colors.84586/)

## Włączanie kompatybilności

### Krok 1

Zainstaluj [ItemsAdderBlocksInjector](https://www.spigotmc.org/resources/itemsadderblocksinjector.102078/) i <mark style="color:red;">nie usuwaj go po instalacji!</mark>.

### Krok 2

Stwórz swój świat Iris (postępuj zgodnie z ich przewodnikami) i użyj identyfikatorów bloków niestandardowych ItemsAdder, tak jak zrobiłbyś to z blokami waniliowymi.

\
Na przykład otwórz ten plik pakietu `overworld`: `plugins\Iris\packs\overworld\biomes\mountain.json`.

Następnie edytuj ustawienia warstw, aby użyć niestandardowego bloku, w tym przykładzie niestandardowego **Amethyst Block**:

```json
"layers": [
    {
        "minHeight": 1,
        "maxPerChunk": 21,
        "maxHeight": 80,
        "minPerChunk": 7,
        "minSize": 3,
        "maxSize": 7,
        "palette": [{ "block": "iasurvival:cassiterite_ore" }],
        "varience": 7
    },
```

Spowoduje to wygenerowanie podobnego wyniku:

![](<../../.gitbook/assets/image (49).png>)

![](<../../.gitbook/assets/image (96).png>)

## Problemy z kompatybilnością.

* FastAsyncWorldEdit przestanie działać, nie mogę nic z tym zrobić.
* WorldEdit `//undo` i `//copy` nie będzie działał z niestandardowymi blokami umieszczonymi przez `Iris`, zostaną one przywrócone do `NOTE_BLOCK` (lub `mushroom`, `TRIPWIRE`, `CHORUS_PLANT`)
