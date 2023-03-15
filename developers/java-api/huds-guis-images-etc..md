# HUDy, GUI...

Aby zobaczyć jak używać HUDów i GUIs API (obrazy czcionek) możesz sprawdzić moje przykłady.

## GUIs

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-GUI" %}

## Huds

{% embed url="https://github.com/LoneDev6/RPGhuds" %}

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-ServerMonitor" %}

### Przykład wartości paska many dostępu

```java
PlayerHudsHolderWrapper huds = new PlayerHudsHolderWrapper(player);
PlayerQuantityHudWrapper manaHud = 
                new PlayerQuantityHudWrapper(huds, "magiccraft:mana_bar");
if(manaHud.exists())
  manaHud.setFloatValue(2.0f);
else
  System.out.println("Error: mana not found, maybe it's disabled.");
```

## FAQ.

{% content-ref url="../../plugin-usage/adding-content/font-images/common-errors.md" %}
[common-errors.md](../../plugin-usage/adding-content/font-images/common-errors.md).
{% endcontent-ref %}

## Pobierz Emoji lub znak GUI

```java
new FontImageWrapper("twitteremojis:confirm").getString()
```
