# ChatControl-Red

[Pobierz tutaj](https://www.mc-market.org/resources/18217/)

Kompatybilność z Emojis:\
Więcej informacji tutaj: [https://github.com/kangarko/ChatControl-Red/issues/853#issuecomment-818497610](https://github.com/kangarko/ChatControl-Red/issues/853#issuecomment-818497610)

## Dodawanie własnego prefiksu kanału w czacie

Jeśli chcesz stworzyć graficzny prefiks dla swoich kanałów i pokazać go na czacie, musisz postępować zgodnie z tym tutorialem.

![Przykład pokazujący prefiks ARCADE dla kanału Arcade](<../../.gitbook/assets/image_(94).png>)

Wystarczy ustawić to w konfiguracji formatu, (na przykład w pliku `format/arcade.yml` programu ChatControl Red):

```yaml
  prefx:
    Message: ':arcade:'
```

Oczywiście trzeba użyć własnej [font\_image](../../plugin-usage/adding-content/font-images/)nazwy zamiast `arcade`, to tylko przykład.
