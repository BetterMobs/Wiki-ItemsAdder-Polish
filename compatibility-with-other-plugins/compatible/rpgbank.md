# RPGBank

## [Pobierz tutaj](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-rpgbank-store-your-items-exp-and-money-using-villagers-npcs-and-custom-gui.29139/)

{% hint style="warning" %}
Musisz mieć zainstalowany [DefaultPack](../../first-install.md#default-pack-optional)!
{% endhint %}

Możesz zmienić ikony GUI i użyć ikon ItemsAdder, aby to osiągnąć:

![](<../../.gitbook/assets/image (13) (1).png>)

{% tabs %}
{% tab title="config.yml" %}
```yaml
  icons:
    money-indicator: coin
    next-page: icon_right_blue
    previous-page: icon_left_blue
    page-indicator: BLACK_STAINED_GLASS_PANE
    deposit-exp: icon_ender_chest
    locked: icon_lock
    deposit-money: icon_arrow_chest
```
{% endtab %}

{% tab title="plik językowy" %}
```yaml
account-title: :offset_-16::blank_menu::offset_-176:&0{player}
```
{% endtab %}
{% endtabs %}
