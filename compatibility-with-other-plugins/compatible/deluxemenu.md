# DeluxeMenu

Aby pokazać element ItemsAdder z niestandardową teksturą na **DeluxeMenu** musisz dodać ten specjalny atrybut do ikony swojego menu:

``yaml
nbt_int: CustomModelData: 1
```

Zamiast 1 musisz ustawić **CustomModelData** swojego niestandardowego elementu.

### Jak uzyskać wartość CustomModelData?

Musisz użyć polecenia `/iatag` trzymając element ItemsAdder, następnie wyszukać wartość `CustomModelData`.
