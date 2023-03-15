# SkinsRestorer

## [Download here](https://www.spigotmc.org/resources/skinsrestorer.2124/)

# How to fix resourcepack not applying on join

### Krok 1

Zainstaluj [**ResourcepackBroadcast**](https://www.spigotmc.org/resources/resourcepackbroadcast.88318/)\NNiech to będzie coś więcej.

### Krok 2

Ustaw w **ResourcepackBroadcast** `config.yml`, aby uruchomić `sr applyskin`, gdy resourcepack jest załadowany poprawnie:

```yaml
success:
  enabled: true
  message:
    enabled: true
    text: "&e%player_name% loaded resourcepack"
  placeholder:
    enabled: true
    text: "%img_smile%"
  commands:
    apply_skin:
      enabled: true
      command: sr applyskin %player_name%
      as_console: true
```
### Krok 3

Otwórz `config.yml` programu **SkinsRestorer** i ustaw `DisableOnJoinSkins: false`.

### Krok 4

Zainstaluj [PlaceholderAPI ](https://www.spigotmc.org/resources/placeholderapi.6245/) (jeśli go nie masz).  
Wykonaj polecenie `/papi ecloud download Player` następnie `/papi reload`.

### Gotowe
