# MODUL 5  - PROAKTIVE KONFLIKTBEHEBUNG

Wir haben bisher zahlreiche neuartige Konzepte beschrieben. Ein auf dem kumulativen Gewicht basierender Konsensmechanismus, der allein durch den Tippauswahlalgorithmus sichergestellt wird, setzt IOTA jedoch weiterhin Miner Wettkämpfen aus.

Um dieses Problem zu lösen, schlagen wir eine zusätzliche Sicherheitsebene vor, auf der Knoten ihre Meinungen durch Abstimmung austauschen. Im Laufe der Jahre wurden umfangreiche Untersuchungen zu Wählermodellen durchgeführt. In Wahrscheinlichkeitsmodellen fordert ein Knoten die Meinung einer kleinen Anzahl anderer Knoten über mehrere Runden an und ändert möglicherweise seine eigene Meinung. In den 70er Jahren wurden die Wählermodelle von Holley / Liggett und Clifford / Sudbury unabhängig voneinander eingeführt (https://projecteuclid.org/euclid.aop/1176996306 und https://academic.oup.com/biomet/article-abstract/60/3/581/217208) / 581/217208), und seitdem hat es eine enorme Menge [verwandter Arbeiten](https://scholar.google.com/scholar?client=ubuntu&channel=fs&oe=utf-8&um=1&ie=UTF-8&lr&cites=196403151939999542) gegeben.

Die Einführung eines **Abstimmungsmechanismus** bringt mehrere Vorteile:

- Anstatt zu warten, bis sich die Situation mit immer mehr ausgegebenen Transaktionen von selbst auflöst, lassen wir die Knoten miteinander sprechen und lösen die Situation proaktiv.

- Das Votum eines Knotens wird nach der Menge an Mana gewichtet, die er besitzt. Daher können gute Mitpsieler einen größeren Einfluss auf das Netzwerk haben.

- Ehrliche Knoten sichern das Netzwerk, indem sie abstimmen, auch wenn sie derzeit keine Transaktionen ausführen. In Kombination mit dem vorgeschlagenen Sybil-Schutzmechanismus (Mana) ersetzt dies die konstante ehrliche Hashing-Kraft in der Blockchain, ohne auf PoW angewiesen zu sein

- Der Konsensprozess ist von anderen Aspekten wie der Auswahl der Tips oder der Struktur des Tangle entkoppelt. Dadurch entsteht ein modulares DLT, das leicht an zukünftige Anforderungen angepasst werden kann. Es verhindert auch alle Formen von Angriffen, die die Struktur des Tangle manipulieren, um den Konsensmechanismus zu brechen, einschließlich der gefährlichsten Angriffe, die im Whitepaper beschrieben werden, wie Parasitenkettenangriffe.

Der Hauptnachteil traditioneller Abstimmungssysteme besteht darin, dass sie nicht sehr gut skalieren. Sie erfordern genaue Kenntnisse aller Netzwerkteilnehmer und haben einen hohen Nachrichtenaufwand.

Wir führen Shimmer ein: ein Abstimmungsschema, das die Probleme der traditionellen Abstimmungsschemata überwindet.

![04_5_shimmer](https://github.com/einfachiota/coordicide/raw/master/assets/04_5_shimmer.gif)

In den folgenden Abschnitten beschreiben wir den aktuellen Stand der Abstimmungsforschung, indem wir zwei Kandidaten für den Abstimmungsaustausch innerhalb von Shimmer vorstellen und erläutern, wie Konsens erzielt werden kann:

- "Cellular Consensus", der das Verhalten in einem Zellularautomaten nachahmt, und
- „Fast Probabilistic Consensus“ (Schneller probabilistischer Konsens), der mithilfe der Wahrscheinlichkeitstheorie starke Sicherheitsgarantien bietet.

### [Nächstes Kapitel](./04_module_5_1)
### [Kapitel zurück](./04_module_4)