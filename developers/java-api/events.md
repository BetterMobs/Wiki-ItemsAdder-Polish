# Events

### ItemsAdderLoadDataEvent

```java
package dev.lone.itemsadder.api.Events;
public class ItemsAdderLoadDataEvent extends Event
```

To zdarzenie jest wywoływane, gdy ItemsAdder załadował poprawnie wszystkie swoje rzeczy (również na `/iareload`).
Posłuchaj tego, aby poczekać, aż wszystkie elementy, obrazy itp. będą dostępne dla twojej wtyczki.

### ResourcePackSendEvent - [docs](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/Events/ResourcePackSendEvent.java)

Zdarzenie wywoływane, gdy serwer wysyła resourcepack do klienta. \
To zdarzenie zawiera **URL**, **hash**, a także zawiera informację, czy **jest to** resourcepack **ItemsAdder** czy **inny plugin** resourcepack.

## Inne wydarzenia

{% embed url="https://github.com/LoneDev6/API-ItemsAdder/tree/master/src/main/java/dev/lone/itemsadder/api/Events" %}
