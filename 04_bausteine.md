# Bausteine

## What are we trying to solve?

Beginnen wir mit zwei grundlegenden Fragen:

- Was versuchen wir zu erreichen, wenn wir von „einem konsensfähigen Netzwerk“ sprechen?
Die Antwort ist eigentlich sehr einfach. Wir möchten, dass alle ehrlichen Knoten dieselbe Meinung über den Status des Ledgers haben. Oder einfacher gesagt, wir möchten, dass alle ehrlichen Knoten vereinbaren, welche Transaktionen gültig sind.

- Da bei IOTA kein "Anführer" gewählt werden muss, um Blöcke zu validieren, über was wird dann eigentlich abgestimmt?
Die Antwort ist wieder relativ einfach. Wenn zwei Transaktionen in Konflikt stehen, führt dies zu einer Aufteilung des Tangles. Um den Konflikt zu lösen, stimmen Knoten über eine bevorzugte Transaktion ab (die nicht bevorzugte Transaktion wird zu einer Waise).

![04_the_modules](https://github.com/einfachiota/coordicide/raw/master/assets/04_the_modules.png)

Herkömmliche PoW-basiertee DLT's bieten eine Reihe von Antworten auf diese Fragen, diese weisen jedoch erhebliche Nachteile auf. Ein PoW-basierter Konsens in IOTA würde Minenrennen einleiten und zu einem erhöhten Stromverbrauch und höheren Kosten führen, wodurch die Verwendung des Netzwerks im IoT eingeschränkt würde.

Eine geeignetere Lösung wird in den folgenden Abschnitten beschrieben.

### [Nächstes Kapitel](./04_module_1.md)
### [Kapitel zurück](./03_modularitaet.md)