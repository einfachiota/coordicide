# MODUL 5  - FAST PROBABILISTIC CONSENSUS

Um den Nachteilen des zellulären Konsenses zu begegnen, analysieren wir gleichzeitig einen weiteren Abstimmungsprozess, für den wir bereits mathematische Modelle und Beweise demonstriert haben: dem Fast Probabilistic Consensus. 

Eine formale Beschreibung des Fast Probabilistic Consensus ist [in diesem Artikel](https://arxiv.org/pdf/1905.10895.pdf) enthalten. Das Grundprinzip ist dem von Cellular Consensus ziemlich ähnlich, aber anstatt asynchron Stimmen zwischen Nachbarn parallel abzugeben, wird der Abstimmungsprozess in separate Runden aufgeteilt. In jeder Runde wählt jeder Knoten eine neue zufällige Untergruppe anderer Knoten aus und fragt deren aktuelle Meinungen ab. Die Meinung eines Knotens wird dann anhand der Mehrheit der zurückgegebenen Meinungen gebildet. Der Begriff der „Mehrheit“ schwankt hier jedoch. Anstatt einen festen Schwellenwert von 50% zu verwenden, verwenden wir einen Entscheidungsschwellenwert, der aus einer [dezentralen Zufallszahlenfolge](https://eprint.iacr.org/2016/228.pdf) abgeleitet wird. Durch Auswahl eines globalen, aber nicht vorhersehbaren Schwellenwerts können wir uns gegen einen Angreifer verteidigen, der den Konsens verzögern möchte.

Dieser Abstimmungsprozess hat die entscheidende Eigenschaft, dass er sehr schnell konvergiert, selbst in Szenarien, in denen böswillige Knoten nach der schlechtesten Strategie abstimmen. Dies wurde im verlinkten Artikel bewiesen, aber das allgemeine Prinzip kann wie folgt erklärt werden:

- Wenn ein Gegner die Entscheidungsregeln kennt, die von ehrlichen Knoten verwendet werden, kann er deren Verhalten vorhersagen und seine Strategie anpassen, um den Prozess auf unbestimmte Zeit anzuhalten.

- Stelle dir eine Situation vor, in der die Schwelle festgelegt ist, ab der ehrliche Knoten ihre Meinung ändern. Jetzt kann ein böswilliger Akteur, der eine ausreichende Anzahl von Knoten kontrolliert, den Anteil seiner Knoten, die angeben, dass sie eine bestimmte Transaktion mochten / nicht mochten, anpassen, um das Netzwerk in einem geteilten (unentschlossenen) Zustand zu halten. Indem wir globale Zufallszahlen verwenden, um diesen Schwellenwert ständig zu ändern, beseitigen wir diese Möglichkeit, indem wir die Regeln konsistent, aber für den Gegner unvorhersehbar machen.

- Es ist daher praktisch unmöglich, das Netzwerk über einen längeren Zeitraum in einem geteilten Zustand zu halten. Es ist wichtig zu beachten, dass diese Zufallszahlen nur dann einen relevanten Einfluss haben, wenn sich das Netzwerk in einem anfänglichen Split-Zustand befindet, und sich nicht auf ein Netzwerk auswirken, das nahe am Konsens liegt.

Nach einer bestimmten Anzahl von Abstimmungsrunden, in denen ein Knoten seine Meinung nicht ändert, kann die Meinung als endgültig betrachtet werden und erfordert keine weitere Abstimmung. Diese Anzahl kann so gewählt werden, dass die Wahrscheinlichkeit, dass das gesamte Netzwerk einen Konsens erreicht hat, beliebig hoch ist.

Aus diesem Grund bietet der Fast Probabilistic Consensus einen Ansatz, mit dem nach einer geringen Anzahl von Runden und mit einer geringen Anzahl von Stichprobenknoten ein Konsens erzielt werden kann, wodurch die erforderlichen Bedingungen für jeden Abstimmungsprozess mit Shimmer erfüllt werden.

### [Nächstes Kapitel](./05_iotas_zukunft.md)
### [Kapitel zurück](./04_module_5_2.md)