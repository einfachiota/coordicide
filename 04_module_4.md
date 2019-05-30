# MODUL 4  - TIP AUSWAHLALGORITHMUS

Der Tippauswahlalgorithmus ist die Methode, mit der Transaktionen zur Genehmigung ausgewählt werden. Ein guter Algorithmus ermöglicht es dem Tangle, stabil und sicher zu wachsen.

![04_4_tangle](https://github.com/einfachiota/coordicide/raw/master/assets/04_4_tangle.gif)

Um eine neue Transaktion an den Tangle anzuhängen, muss der Algorithmus zwei vorherige Transaktionen auswählen und genehmigen - vorzugsweise Tipps. Dieser Genehmigungsmechanismus repräsentiert den „Glauben“ an den Tangle: Wenn die Transaktion y die Transaktion x genehmigt, bedeutet dies, dass y glaubt, dass die Transaktion x gültig ist und dass auch ihre gesamte Historie gültig ist.

![04_4_reliabale2](https://github.com/einfachiota/coordicide/raw/master/assets/04_4_reliabale2.png)

In der Vergangenheit haben wir einen voreingenommenen "random walk" als Tippauswahl-Algorithmus verwendet, da dies nicht nur zu einer gesunden Tangle-Struktur führte, sondern uns auch die Identifizierung des schwersten und daher bevorzugten Teils des Tangle ermöglichte. Dieser Mechanismus war zwar für das Erreichen eines Konsenses von wesentlicher Bedeutung, zeigte jedoch auch Eigenschaften, die weniger wünschenswert waren:

- Ehrliche Transaktionen könnten zurückbleiben, wenn sie nicht genug Gewicht ansammeln würden. Dies führte zu einem erhöhten Bedarf an "promotions" und "reattachments" (auch ohne Angriffe), was wiederum die Zuverlässigkeit von Transaktionen erheblich verringerte.
- Angreifer könnten versuchen, das Eindringen in böswillige Strukturen wie parasitäre Ketten zu „spielen“, oder das Netzwerk daran hindern, einen Konsens zu erzielen, indem sie Splitting-Angriffe ausführen.
- Die Berechnung der kumulativen Gewichte von Transaktionen ist relativ teuer und stellt ein Problem für die Skalierbarkeit des Protokolls dar, insbesondere in Szenarien mit hohem Durchsatz.

Durch Hinzufügen einer Abstimmungsschicht zur Identifizierung des bevorzugten Teils des Tangles (als zusätzliches Modul) sind wir in der Lage:

- Es löst die Konflikte viel schneller und verringert daher die Wahrscheinlichkeit, dass eine Transaktion versehentlich mit dem falschen Teil des Tangles verknüpft wird.

- Es werden verschiedene Tippauswahlmechanismen verwendet, die nicht mehr auf dem kumulierten Gewicht basieren und eine geringere Wahrscheinlichkeit haben, gültige Transaktionen zurückzulassen.

![04_4_reliabale1](https://github.com/einfachiota/coordicide/raw/master/assets/04_4_reliabale1.png)

Dies wird die Zuverlässigkeit von Transaktionen im IOTA-Netzwerk erhöhen und den Bedarf an "reattachments" und "promotions" erheblich verringern. Dadurch wird auch die Auswahl der Tipps viel effizienter.

### [Nächstes Kapitel](./04_module_5_0)
### [Kapitel zurück](./04_module_3)