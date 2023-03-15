# AnimatedScoreboard

## [Pobierz tutaj](https://www.spigotmc.org/resources/animatedscoreboard.20848/)

{% hint style="warning" %}
Proszę zapoznać się z tutorialami na stronie wtyczki przed zwróceniem się o pomoc, nie jestem twórcą tej wtyczki i ta informacja może stać się nieaktualna w pewnym momencie.
{% endhint %}

## Obrazy czcionek w tabeli wyników

Możesz użyć [font\_images ](../../plugin-usage/adding-content/font-images/)(emotki i symbole) w tabeli wyników, jeśli zainstalujesz **PlaceholderAPI**.

### Przykład

`%img_smile%` będzie wyglądał tak:

![](../../.gitbook/assets/animatedscoreboard\_1.png)

## Ukryj tło tablicy wyników

Dzięki ItemsAdder możesz ukryć tło tablicy wyników, wystarczy użyć tej sztuczki.

(działa z każdą wtyczką tablicy wyników, która obsługuje PlaceholderAPI)

{% tabs %}
{% tab title="Przed" %}
​

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-M28TcKgSDvuFN510qye%2F-MhOfUmIRJYMhFZM2AQy%2F-MhOgJ6DpHjDR8dc9NYc%2Fimmagine.png?alt=media&#x26;token=1a5efcc3-27a5-49b4-80c9-c98ebcb197d2" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Po" %}
​\\

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-M28TcKgSDvuFN510qye%2F-MhOfUmIRJYMhFZM2AQy%2F-MhOg9VxfKvE2ZGZ3QE6%2Fimmagine.png?alt=media&#x26;token=c4ee2fd0-2aa9-46e2-a8dd-0025dcc64f7e" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Jak ukryć tło

Wystarczy dodać `%img_offset_-500%` przed <mark style="color:yellow;">**każdą linią**</mark> swojej konfiguracji tablicy wyników, <mark style="color:yellow;">nawet w pustych liniach!</mark>.

{% hint style="danger" %}
#### Ostrzeżenie!

Niekompatybilne ze specjalnymi atrybutami **AnimatedScoreboard** jak te i podobne!

`<health full=&4 half=&c empty=&f update=5>❤</health>`

`<repeat times=10>|</repeat>`

`<stay ticks=100>&lAnimated Scoreboard</stay>`

<mark style="color:red;">Proszę nie prosić mnie o wsparcie</mark>, nie mogę tego naprawić, nie jestem autorem **AnimatedScoreboard**.

Jeśli chcesz użyć `<stay>` musisz umieścić `%img_offset_-500%` po pierwszym `>`.‖.
Przykład:

`<stay ticks=100>%img_offset_-500%&lAnimated Scoreboard</stay>`
{% endhint %}

<details>

<summary>&#x3C;--- Kliknij tutaj, aby uzyskać przykładowy plik konfiguracyjny YML</summary>

{% code title="defaultscoreboard.yml" %}
```yaml
display:
    title:
      text:
      - "%img_offset_-500%&lA"
      - "%img_offset_-500%&lAn"
      - "%img_offset_-500%&lAni"
      - "%img_offset_-500%&lAnim"
      - "%img_offset_-500%&lAnima"
      - "%img_offset_-500%&lAnimat"
      - "%img_offset_-500%&lAnimate"
      - "%img_offset_-500%&lAnimated"
      - "%img_offset_-500%&lAnimated "
      - "%img_offset_-500%&lAnimated S"
      - "%img_offset_-500%&lAnimated Sc" 
      - "%img_offset_-500%&lAnimated Sco"
      - "%img_offset_-500%&lAnimated Scor"
      - "%img_offset_-500%&lAnimated Score"
      - "%img_offset_-500%&lAnimated Scoreb"
      - "%img_offset_-500%&lAnimated Scorebo"
      - "%img_offset_-500%&lAnimated Scoreboa"
      - "%img_offset_-500%&lAnimated Scoreboar"
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"     
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"
      - "<stay ticks=100>%img_offset_-500%&lAnimated Scoreboard</stay>"
      random: false
      interval: 2
    line-1:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 200
      score: 99   
    line-2:
      text:
      - "%img_offset_-500%&a&lWelcome %player_name%"
      - "%img_offset_-500%&b&lWelcome %player_name%"
      - "%img_offset_-500%&c&lWelcome %player_name%"   
      random: false
      interval: 5
      score: 98
    line-3:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 20
      score: 97
    line-4:
      text:
      - "%img_offset_-500%&aYour gamemode:"
      - "%img_offset_-500%&aYour location:"
      - "%img_offset_-500%&aYour world:"    
      random: false
      interval: 60
      score: 96
    line-5:
      text:
      - "%img_offset_-500% &b%player_gamemode%"
      random: false
      interval: 60
      score: 95
    line-6:
      text:
      - "%img_offset_-500% &bX:%player_x% Y:%player_y% Z:%player_z%"
      random: false
      interval: 1
      score: 95
    line-7:
      text:
      - "%img_offset_-500% &b%player_world%"    
      random: false
      interval: 60
      score: 95
    line-8:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 200
      score: 95
    line-9:
      text:
      - "%img_offset_-500%&1Random Rotation"
      - "%img_offset_-500%&2Random Rotation"
      - "%img_offset_-500%&3Random Rotation"
      - "%img_offset_-500%&4Random Rotation"
      - "%img_offset_-500%&5Random Rotation"
      - "%img_offset_-500%&6Random Rotation"
      - "%img_offset_-500%&7Random Rotation"
      - "%img_offset_-500%&8Random Rotation"
      - "%img_offset_-500%&9Random Rotation"
      - "%img_offset_-500%&aRandom Rotation"
      - "%img_offset_-500%&bRandom Rotation"
      - "%img_offset_-500%&cRandom Rotation"
      - "%img_offset_-500%&dRandom Rotation"
      - "%img_offset_-500%&eRandom Rotation"
      - "%img_offset_-500%&kRandom Rotation" 
      - "%img_offset_-500%&lRandom Rotation" 
      - "%img_offset_-500%&mRandom Rotation" 
      - "%img_offset_-500%&nRandom Rotation"
      - "%img_offset_-500%&oRandom Rotation"
      - "%img_offset_-500%&rRandom Rotation"       
      random: true
      interval: 1
      score: 94
    line-10:
      text:
      - "%img_offset_-500%"       
      random: true
      interval: 1
      score: 93
```
{% endcode %}

</details>
