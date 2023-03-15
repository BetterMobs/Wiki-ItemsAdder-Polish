---
description: Emoty mają zbugowane tekstury (1.17+)
---

# 💃 Zepsute tekstury emotów

## Problemy z modami shaderowymi

Mody, które pozwalają na używanie niestandardowych shaderów będą łamać emotki z powodu ich nadpisywania/zastępowania waniliowego shadera, którego ItemsAdder używa do funkcji Emotes.

Jedynym sposobem na _"naprawienie"_ tego jest wyłączenie samych shaderów lub usunięcie danego moda.

{% tabs %}
{% tab title="Z włączonymi shaderami (błąd)" %}
![shader bug](<../.gitbook/assets/image (51) (2) (1).png>)
{% endtab %}

{% tab title="Z wyłączonymi shaderami (bez błędu)" %}
![brak błędu z shaderami](<../.gitbook/assets/image (64).png>)
{% endtab %}
{% endtabs %}

Znane mody shaderów, które powodują problemy:

### Optifine

Powiązany problem: [https://github.com/sp614x/optifine/issues/6391](https://github.com/sp614x/optifine/issues/6391)

### IrisShaders

Related issue: [https://github.com/IrisShaders/Iris/issues/1042](https://github.com/IrisShaders/Iris/issues/1042)

## Mody zmieniające skórki graczy

Mod może zmienić domyślny model/skórę gracza i dlatego może być dotknięty przez manipulacje shaderów ItemsAddera, lub odwrotnie.

Znane mody, które powodują problemy:

### 3DSkinLayers

Mod zmienia zewnętrzną warstwę skóry, aby wyglądała w 3D, co zmienia sam model gracza.

Możliwą poprawką jest wyłączenie `3D Skulls` i `3D Skull Items` w ustawieniach moda.
Obecnie nie ma obejścia dla używania warstw 3D w animacjach Emote.

Dodatkowe informacje można znaleźć w powiązanym problemie: [https://github.com/tr7zw/3d-Skin-Layers/issues/45](https://github.com/tr7zw/3d-Skin-Layers/issues/45)

### Dostosowywalne modele graczy

Ten mod pozwala na pełną personalizację modelu gracza, włączając w to wymianę jego części lub całego modelu.
Z tego powodu Emoty nie będą wyświetlane poprawnie w ItemsAdder i nie ma obecnie żadnej dostępnej poprawki poza nieużywaniem moda lub nieużywaniem animacji Emote.
