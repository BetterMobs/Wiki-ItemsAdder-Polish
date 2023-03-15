# ExecutableItems

## [Pobierz tutaj](https://www.spigotmc.org/resources/custom-items-free-executable-items-1-12-1-17.77578/)

## Jak podłączyć ExecutableItem do elementu ItemsAdder

{% hint style="warning" %}
ZAKTUALIZUJ **ITEMSADDER** DO WERSJI **2.2.20+**.
UPDATE **ExecutableItems** to **4.2.3.5+**.
{% endhint %}

## Tworzenie elementu ItemsAdder

### Utwórz swój plik .yml jak zwykle i dodaj wszystkie właściwości dla elementu ItemsAdder

W tym przykładzie podłączę element **ItemsAdder** o nazwie `executableitem_test` do przykładowego elementu `spit` z plików przykładowych ExecutableItem.

```yaml
info:
  namespace: example
items:
  executableitem_test:
    display_name: executableitem_test
    permission: executableitem_test
    executableitem:
      id: Free_Spit
    resource:
      material: IRON_INGOT
      generować: true
      tekstury:
      - item/executableitem_test.png
    durability:
      max_custom_durability: 1324
```

{% hint style="success" %}

Są one używane do **połączenia** dwóch elementów**.
{% endhint %}

### Pobierz element

Uruchom `/iaget executableitem_test` i uzyskaj element!

![](<../../.gitbook/assets/image_(140) (1) (1).png>)
