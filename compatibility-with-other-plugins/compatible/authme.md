# Authme

## [Pobierz tutaj](https://www.spigotmc.org/resources/authmereloaded.6269/)

## Jak zastosować resourcepack po zalogowaniu

Otwórz **config.yml** z **ItemsAdder** i wyłącz `apply-on-join`.

```yaml
resource-pack:
  apply-on-join: false
```

Otwórz `commands.yml` z **Authme** i zmień `onLogin` na to:

```yaml
onLogin:
  apply_pack:
    command: 'iatexture %p'
    executor: CONSOLE
```

{% hint style="warning" %}
Upewnij się, że w pliku konfiguracyjnym jest **tylko jedno ustawienie onLogin**.
{% endhint %}
