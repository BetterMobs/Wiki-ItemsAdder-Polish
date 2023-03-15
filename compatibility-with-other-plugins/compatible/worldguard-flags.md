---
opis: Lista flag Worldguard.
---

# WorldGuard

## Flags list

### ia-furniture-sit

Ta flaga pozwala graczom siedzieć na meblach lub nie (meble z `furniture_sit` [behaviour](../../plugin-usage/adding-content/item-properties/behaviours.md))

### ia-campfire-item-add

Umożliwienie użytkownikowi przeniesienia przedmiotu do ogniska

### ia-campfire-item-remove

Pozwala użytkownikowi usunąć przedmiot z ogniska

### ia-vehicle-place

Pozwala użytkownikowi na umieszczenie pojazdów w regionie

### ia-vehicle-remove

Pozwala użytkownikowi na usunięcie KAŻDEGO pojazdu w regionie

### ia-vehicle-personal-remove

pozwala użytkownikowi na usuwanie tylko jego własnych pojazdów w regionie

### ia-vehicle-sit

Pozwala użytkownikowi usiąść na dowolnym pojeździe w regionie

### ia-vehicle-personal-sit

pozwala użytkownikowi siedzieć tylko na własnych pojazdach w regionie

### ia-trade-machine-use

zezwala użytkownikowi na korzystanie z maszyn handlowych

### ia-placed-block-interact

pozwala użytkownikowi na wyzwalanie zdarzeń typu placedblock.interact

### ia-placed-armorstand-interact

pozwala użytkownikowi na wyzwalanie zdarzeń interakcji z placed_armorstand.interact

{% hint style="info" %}
Ustaw **iając **ia-vehicle-sit** na Deny i **ia-vehicle-personal-sit** na Allow, aby gracze mogli siedzieć tylko na osobistych pojazdach.
{endhint %}

## Częste problemy

{% hint style="warning" %}
Jeśli twoi użytkownicy **nie mogą siedzieć** na **pojazdach**, nawet jeśli ustawiłeś odpowiednią flagę:

* sprawdź, czy używasz regionu `__global__` jako swojego głównego regionu (tego, na którym zastosowałeś flagę furniture). Jeśli tak, proszę utworzyć nowy region. region globalny jest znany z tego, że daje pewne problemy z niektórymi flagami wtyczek.
* sprawdź, czy ustawiłeś flagę `build` lub `passthrough`. \
  Pamiętaj, że tych flag nie wolno zmieniać, powinieneś zachować wartość domyślną (niezaznaczony, szary tekst)
{% endhint %}
