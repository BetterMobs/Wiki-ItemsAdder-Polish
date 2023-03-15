# Scoreboard-revision

## [Pobierz tutaj](https://www.spigotmc.org/resources/scoreboard.14754/) <a href="#download-here" id="download-here"></a>.

{% hint style="warning" %}
Wygląda na to, że plugin został usunięty z jakiegoś powodu ze SpigotMC.org.
( Nie jestem jego autorem).

[Source code](https://github.com/RienBijl/Scoreboard-revision)
{% endhint %}

## Obrazy czcionek

Możesz użyć [font_images ](../../plugin-usage/adding-content/font-images/)(emojis i symbole) w **scoreboard**.

### Przykład.

`%img_smile%` pokaże się tak:

![](../../.gitbook/assets/image\_\(95\).png)

## Ukryj tło tablicy wyników

( działa z każdym pluginem scoreboardowym)

### Przed

![](../../.gitbook/assets/image\_\(97\).png)

### Po

![](../../.gitbook/assets/image\_\(96\).png)

Za pomocą ItemsAdder możesz ukryć tło tablicy wyników, wystarczy użyć tej sztuczki.\N
Wystarczy dodać `%img_offset_-500%` przed <mark style="color:yellow;">**każdą linią**</mark> swojej konfiguracji tablicy wyników, <mark style="color:yellow;">nawet w pustych liniach!</mark>.

```yaml
# ____ ____ ____ ____ _____ ____ ____ ____ ____ ____
# / ___\/ _\/ _ \/ __\/ __// _ \/ _ \/ _ \/ __\/ _ \
# | \| / | / \|| \/|| \ | | //| / \|| / \|| \/|| | \|
# \___ || \_ | \_/|| /| /_ | |_\\| \_/|| |-||| /| |_/|
# \____/\____/\____/\_/\_\\____\\____/\____/\_/ \|\_/\_\\____/
#
# Scoreboard-r by Rien Bijl
# rep: github : RienBijl/Scoreboard-revision
# v: R4 1.1 RELEASE

# Nie edytuj! Plugin używa tego do określenia czy konfiguracja jest odpowiednia
config_version: 1

settings:
  # Sterownik to implementacja tablicy wyników używana do wyświetlania użytkownika
  # Stare sterowniki będą od teraz wspierane, tak że powrót do
  # starszą (być może bardziej stabilną) wersję jest łatwe.
  driver: SCOREBOARD_DRIVER_V1
  # Czy powinniśmy sprawdzić aktualizacje? Uwaga! Wyłączenie tego nie jest zalecane
  # możesz przegapić świetne aktualizacje *wink*
  check-updates: true

# W jakich światach powinniśmy wyłączyć tablicę wyników?
disabled-worlds:
  - 'non_existant_world'

board:
  title:
    interval: 3
    lines:
      - '%img_offset_-500%&4> &c&lScoreboard-r &4<'
      - '%img_offset_-500%&4> &c&lScoreboard &4<'
      - '%img_offset_-500%&4> &c&lcoreboar &4<'
      - '%img_offset_-500%&4> &c&loreboa &4<'
      - '%img_offset_-500%&4> &c&leb &4<'
      - '%img_offset_-500%&4> &4<'
      - '%img_offset_-500%&4> &c&leb &4<'
      - '%img_offset_-500%&4> &c&loreboa &4<'
      - '%img_offset_-500%&4> &c&lcoreboar &4<'
      - '%img_offset_-500%&4> &4&lScoreboard &4<'
      - '%img_offset_-500%&4> &4&lScoreboard-r &4<'
      - '%img_offset_-500%&4> &c&lScoreboard-r &c&o4 &4<'
      - '%img_offset_-500%&4> &4&lScoreboard-r &4&o4 ツ &4<'
      - '%img_offset_-500%&4> &c&lScoreboard-r &c&o4 ツ &4<'
      - '%img_offset_-500%&4> &4&lScoreboard-r &4&o4 ツ &4<'
      - '%img_offset_-500%&4> &c&lScoreboard-r &c&o4 ツ &4<'
      - '%img_offset_-500%&4> &c&lScoreboard-r &c&o4 &4<'
  rows:
    1:
      interval: 5
      lines:
        - '%img_offset_-500%&c------------------------'
        - '%img_offset_-500%&4------------------------'
    2:
      interval: 80
      lines:
        - '%img_offset_-500%&cPlayer &4&l> &f%img_smile%'
    3:
      interval: 80
      lines:
        - '%img_offset_-500%%player_name%'
    4:
      interval: 80
      lines:
        - '%img_offset_-500%&4♡ &f&o%player_health_rounded%/%player_max_health_rounded%'
        - '%img_offset_-500%%player_ping% &7ms latency'
    5:
      interval: 80
      lines:
        - '%img_offset_-500%'
    6:
      interval: 80
      lines:
        - '%img_offset_-500%&cServer &4&l>'
    7:
      interval: 80
      lines:
        - '%img_offset_-500%%server_unique_joins% &7unique players'
        - '%img_offset_-500%%server_online% &7online players'
    8:
      interval: 80
      lines:
        - '%img_offset_-500%%server_ram_used%mb/%server_ram_total%mb &7ram usage'
        - '%img_offset_-500%%server_tps_1% &7ticks per second'
    9:
      interval: 5
      lines:
        - '%img_offset_-500%&c------------------------'
        - '%img_offset_-500%&4------------------------'
```
