# RealisticWorldGenerator

## [Pobierz tutaj](https://www.spigotmc.org/resources/realisticworldgenerator-1-8-8-1-16-x.15905/)

## Kompatybilność

* biomy
* rudy
* schematy (schematy RWG)

{% hint style="warning" %}
To działa tylko na ItemsAdder 2.5.2+ i RealisticWorldGenerator 4.30+.
{% endhint %}

## Ostrzeżenia

{% hint style="danger" %}
Nie używaj niestandardowych bloków jako bloków rud bazowych. To spowoduje zbyt duży lag.\N
Nadal używaj do tego celu bloków waniliowych.
{% endhint %}

{% code title="ores.yml" %}
```yaml
rudy:
  veins:
    biome_layers:
      paste: false
    type: 1
    włączony: true
  base:
    block: ia:itemsadder:ruby_block # <---- DO NOT DO THIS!
```
{% endcode %}

{% hint style="success" %}
Używaj niestandardowych bloków tylko dla:

* powierzchni.
* rudy
* struktur (schematów)
{% endhint %}

## Jak używać niestandardowych bloków

Dla przykładu stwórzmy biome, który ma rubinowy blok jako górną warstwę.

Otwórz plik `biomes.yml` w swoim folderze konfiguracyjnym świata **RealisticWorldGenerator**.

Zdecyduj się na biome (na przykład `plains`) i dodaj to jako pierwszą warstwę.

{% code title="biomes.yml" %}
```yaml
równiny:
  layer:
    '1':
    - ia:itemsadder:ruby_ore;120
    '2':
    - minecraft:coarse_dirt;2
    - minecraft:podzol[snowy=false];5
    - minecraft:grass_block[snowy=false];100
```
{% endcode %}

W tym przykładzie zmodyfikowałem również plik `settings.yml` tego świata, aby upewnić się, że generowany jest tylko biome, aby łatwiej znaleźć moje niestandardowe bloki.

{% code title="settings.yml" %}
```yaml
one_biome:
  biome: PLAINS
  oceany: false
  enabled: true
```
{% endcode %}

### Oto końcowy rezultat

To jest świat z niestandardową powierzchnią

![](<../../.gitbook/assets/image (41) (1).png>)


