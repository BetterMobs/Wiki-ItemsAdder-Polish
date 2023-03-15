# Graves

## [Pobierz tutaj](https://www.spigotmc.org/resources/graves.74208/)

## Jak dodać kompatybilność?

Włącz kompatybilność

```yaml
itemsadder: # https://www.spigotmc.org/resources/itemsadder.73355/
  enabled: true # Czy integracja ItemsAdder powinna być włączona.
```

Edytuj domyślną opcję. Możesz również dostosować przedmioty w razie potrzeby (upewnij się, że są one właściwego typu, użyj mebli w meblach i użyj bloku we właściwości bloku).

```yaml
  ##############
  # ItemsAdder #
  ##############
  # The option requires ItemsAdder, you must have this installed to use models.
  itemsadder:
    furniture:
      enabled: true # Should we use ItemsAdder Furniture?
      name: "itemsadder:mysterious_stone" # Furniture name.
    block:
      enabled: true # Should we use ItemsAdder Blocks?
      name: "itemsadder:nice_stone" # Block name
```
