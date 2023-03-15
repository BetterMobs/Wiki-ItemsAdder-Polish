---
description: Jak zainstalować plugin
---

# ⚙ Pierwsza instalacja

{% hint style="info" %}
**Powiniejeś śledzić** tą pierwszą konfigurację **na** twoim **serwerze testowym** na twoim PC, aby **unikać pomyłek** i dużej ilości restartów.. Gracze nie lubią kiedy serwer jest Offline.\
Możesz wysłać po konfigurajci pliki na serwer
{% endhint %}

{% hint style="danger" %}
**Upewnij się** , że wszystkie pluginy na serwerze muszę być zaktualizowane!
{% endhint %}

## Step 1 - Instalacja pluginu i bibliotek

* zatrzymaj serwer
* zainstaluj [**ProtocolLib**](https://ci.dmulloy2.net/job/ProtocolLib/lastSuccessfulBuild/)
* zainstaluj [**LoneLibs**](https://www.spigotmc.org/resources/lonelibs.75974/)
* wsadź plik `ItemsAdder.jar` do środka twojego folderu pluginów "plugins"
* uruchom serwer
* pozwól ItemsAdderowi ustawić **wszystko**

Pierwszy krok jest zrobiony.

{% hint style="warning" %}
Teraz musisz ukończyć **krok drugi** ,aby skonfigurować paczkę zasobów (spokojnie, nie jest to bardzo trudne).\
<mark style="color:red;">**NIE POMIJAJ!**</mark>
{% endhint %}

## Krok 2 - Pierwsza instalacja paczki zasobów

{% hint style="warning" %}
Ten krok jest ważny, plugin <mark style="color:red;">**NIE BĘDZIE DZIAŁAŁ**</mark> jeśli nie skończysz tego kroku!
{% endhint %}

Przed użyciem pluginu, zadecyduj jaki sposób hostingu paczki zasobów wybierzesz. \
Kliknij tutaj, aby zadecydować o metodzie hostowania paczki zasobów (najlepsza metoda: `self-host`).

{% content-ref url="plugin-usage/resourcepack-hosting/" %}
[resourcepack-hosting](plugin-usage/resourcepack-hosting/)
{% endcontent-ref %}

## Step 3 - (opcjonalne) Dodaj oficjalne zasoby ItemsAddera

![](.gitbook/assets/items\_showcase\_gif.apng)

**ItemsAdder** jest w zestawie z fajnymi zasobami gotowymi dla ciebie.\
Nie jest to automatycznie zawarte w pobranej wtyczce, ponieważ niektórzy ludzie mogą nie chcieć, aby każdy przedmiot / funkcja została automatycznie dodana do ich serwera.
### Standardowa paczka (opcjonalne)

![](<.gitbook/assets/image (47).png>)

* Pobierz najnowszą wersję standardowej paczki: **DefaultPack**: [POBIERZ](https://github.com/ItemsAdder/DefaultPack/releases/latest)
* Wypakuj zawartość do folderu `ItemAdder` i nadpisz każdy plik, jeśli będziesz o to zapytany
* Uruchom komendę `/iazip` (i podożaj za poradami odnośnie swojej [metody hostingu](plugin-usage/resourcepack-hosting/) jeżeli nie korzystasz z **self-host**).

### Inne paczki (opcjonalne)

![](<.gitbook/assets/image (50).png>)

* jeśli chcesz możesz pobrać inną paczkę: **OtherPack** które dodają jeszcze więcej rzeczy: [POBIERZ](https://github.com/ItemsAdder/OtherPacks/releases/latest)
* Wypakuj zawartość do folderu `ItemAdder` i nadpisz każdy plik, jeśli będziesz o to zapytany
* Uruchom komendę `/iazip` (i podożaj za poradami odnośnie swojej [metody hostingu](plugin-usage/resourcepack-hosting/) jeżeli nie korzystasz z **self-host**).

Jeżeli korzystasz z wersji 1.17 lub niższej musisz to zmienić w generowaniu ród:

* Otwórz te pliki i ustaw `enabled: true`.
  * `contents\iaalchemy\configs\worlds_populators_old.yml`
  * `contents\iasurvival\ores\configs\worlds_populators_old.yml`
* Otwórz te pliki i ustaw `enabled: false`.
  * `contents\iaalchemy\configs\worlds_populators_1_18.yml`
  * `contents\iasurvival\ores\configs\worlds_populators_1_18.yml`

### Usuwanie standardowych rzeczy (opcjonalne)

{% content-ref url="faq/removing-default-stuff/" %}
[removing-default-stuff](faq/removing-default-stuff/)
{% endcontent-ref %}
