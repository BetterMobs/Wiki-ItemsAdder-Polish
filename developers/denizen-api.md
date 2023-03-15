# 📓 Denizen API

{% hint style="warning" %}
Wymaga ItemsAdder 3.2.4+
{% endhint %}

## Pobierz najnowszy build

{% embed url="https://ci.citizensnpcs.co/job/Denizen/" %}

## Funkcje

<pre class="language-yaml"><code class="lang-yaml"><strong># Sprawdza czy item jest customowy
</strong><strong>player.item_in_hand.is_ia_item
</strong># Sprawdza, czy przedmiot jest niestandardowym blokiem
player.item_in_hand.is_ia_block
# Zdobądź identyfikator elementu
player.item_in_hand.ia_namespaced_id

# Umieść blok niestandardowy.
# Składnia set_custom_block [&#x3C;location>|...] [&#x3C;namespaced_id>]
set_custom_block &#x3C;context.location> ruby_block 
# Sprawdź czy blok jest blokiem niestandardowym
context.location.is_ia_block
# Zdobądź identyfikator bloku z nazwą
context.location.ia_namespaced_id</code></pre>

## Przykład

```yaml
my_world_script:
    type: world
    events:
        after player left clicks block:
            - narrate " "
            - if <player.item_in_hand.is_ia_block>:
                - narrate "Left click item is a custom block! <&6><player.item_in_hand.ia_namespaced_id>"
            - else:
                - narrate "Left click item is NOT a custom block! <&7><player.item_in_hand.material>"
            - narrate " "
        after player right clicks block:
            - if <player.is_sneaking>:
                - set_custom_block <context.location> ruby_block 
            - else:
                - narrate " "
                - if <player.item_in_hand.is_ia_item>:
                    - narrate "Right click item is a custom item! <&6><player.item_in_hand.ia_namespaced_id>"
                - else:
                    - narrate "Right click item is NOT a custom item! <&7><player.item_in_hand.material>"

                - if <context.location.is_ia_block>:
                    - narrate "Interacted block is a custom block! <&6><context.location.ia_namespaced_id>"
                - else:
                    - narrate "Interacted block is NOT a custom block!"
                - narrate " "
```
