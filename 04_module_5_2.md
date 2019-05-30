# MODUL 5  - CELLULAR CONSENSUS

In Cellular Consensus wird der Abstimmungsprozess als zellularer Automat modelliert, bei dem Knoten als Zellen betrachtet werden können, die die Zustände ihrer Nachbarn überwachen und ihre Meinung entsprechend anpassen. Der eigentliche Konsensalgorithmus ist äußerst einfach und kann in 5 Codezeilen zusammengefasst werden:

```javascript
If NumberOfNeighborsPreferringTransaction(tx) > NumberOfNeighbors / 2 {
    PreferTransaction(tx)
} else {
    DislikeTransaction(tx)
}
```

Dies beschreibt einen Mechanismus, bei dem Knoten die Mehrheitsmeinung ihrer Nachbarn übernehmen und eine auf dieser Mehrheit basierende Transaktion mögen oder ablehnen.

Es ist extrem schnell und robust. Die folgende Animation zeigt eine Simulation von 10.000 Knoten, die bei 128 in Konflikt stehenden Transaktionen einen Konsens erzielen (verschiedene Farben stehen für verschiedene Transaktionen):

![04_5_2_module_5.1.1](https://github.com/einfachiota/coordicide/raw/master/assets/04_5_2_module_5.1.1.gif)

In diesem Beispiel erreicht das Netzwerk innerhalb von Sekunden einen Konsens.

Das Erhöhen der Anzahl der Knoten wirkt sich auf die Zeit aus, die für die Übertragung von Transaktionen im Netzwerk benötigt wird, nicht jedoch auf die Zeit, um einen Konsens zu erzielen. Entscheidungen werden lokal und parallel getroffen, unabhängig davon, wie viele Knoten am Netzwerk beteiligt sind.

Die Tatsache, dass Abstimmungen immer mit denselben Nachbarn ausgetauscht werden, kann einen Angriffsweg darstellen. Wir erhöhen die Sicherheit, indem wir die manabasierte Reputation in den Peering-Prozess einbeziehen: Knoten bevorzugen Nachbarn mit einer ähnlichen Reputation. Dies macht es für Angreifer sogar teuer, als Nachbarn betrachtet zu werden, und es ist ein weiterer Anreiz für Knoten, ein hohes Ansehen zu erlangen. Das Netzwerk wird zunehmend sicherer, da die Menge an Mana, die ehrliche Knoten besitzen, mit der Zeit auf natürliche Weise zunimmt.

## Sprich über die Meinung: Das Immunsystem des Organismus

Durch die Behandlung von Knoten als Zellen eines lebenden Organismus können wir ein „Immunsystem“ implementieren. Dies schützt das Netzwerk vor Angriffen, indem die Teilnehmer gezwungen werden, sich an die Regeln zu halten, und bietet einen besseren Schutz als herkömmliche Maßnahmen wie den Schutz von Sybil. Da alle Nachbarn zufällig ausgewählt werden, ist der Prozess, mit dem Shimmer einen Konsens erzielt, höchst wahrscheinlich. Auf Knotenebene ist der zelluläre Konsens jedoch deterministisch. Auf diese Weise können wir das Verhalten eines Knotens überprüfen, wenn wir die Meinung seiner Nachbarn kennen. Schlechte Akteure, die gegen die Regeln verstoßen, können daher (wie unten gezeigt) von jedem ihrer Nachbarn sofort erkannt und vertrieben werden.

![04_5_2_gossip.gif](https://github.com/einfachiota/coordicide/raw/master/assets/04_5_2_gossip.gif)

Diese Idee kann in dem folgenden Protokoll, das wir "Sprich über die Meinung" nennen, formalisiert werden:

- In regelmäßigen Abständen sendet jeder Knoten eine "Herzschlag" ("Heartbeat") -Nachricht an seine Nachbarn. Dies beinhaltet seine aktuelle Meinung und den Grund, warum es zu dieser Meinung gekommen ist, d. H. Die Meinungen seiner Nachbarn in der vorherigen Runde.

- Um die Menge der ausgetauschten Daten zu komprimieren, wird nur die Differenz zwischen aufeinanderfolgenden Herzschlägen gesendet, d. H. Nur die Transaktions-Hashes, deren Status "Gefällt mir" geändert wurde.

- Ein Knoten signiert seine Herzschlag-Nachrichten und Meinungen, um die Authentizität zu gewährleisten.

Dieser Herzschlag dient mehreren Zwecken:

- Es zwingt Knoten, regelmäßige Aussagen zu treffen und aktive Mitglieder des Netzwerks zu bleiben.

- Es wird verwendet, um Meinungen zwischen Nachbarn zu synchronisieren, sodass Knoten ihre eigene Meinung gemäß den zuvor beschriebenen Regeln aktualisieren können, ohne proaktiv andere Knoten abfragen zu müssen.

- Auf diese Weise können Knoten überprüfen, ob ihre Nachbarn ehrlich sind - diejenigen, die gegen das Protokoll verstoßen, indem sie ihre Meinung ändern, können sofort aus dem Netzwerk entfernt werden. Da die Nachrichten signiert sind, kann ein Fehlverhalten nachgewiesen werden, indem böswillige Nachrichten auf die Knoten zurückverfolgt werden, von denen sie ausgegeben wurden.

Dieser Ansatz weist eine Reihe von überzeugenden Merkmalen auf, die in keinem anderen erlaubnislosen Konsensmechanismus zu finden sind: seine asynchrone Natur, die Einfachheit seiner Implementierung, die Effizienz seines Nachrichten-Overheads, die Geschwindigkeit, mit der er einen Konsens erreicht, und seine Angriffsresistenz.

Während emergente Phänomene in biologischen Systemen weit verbreitet sind und sich in der Praxis bewährt haben, ist es äußerst schwierig, sie mathematisch zu modellieren, da sie von Natur aus chaotisch und komplex sind. Der größte Nachteil des Ansatzes ist daher die Komplexität der Formalisierung seiner wissenschaftlichen Beweise. Es wäre notwendig, Cellular Consensus in einer Testnetzumgebung gründlich zu untersuchen, bevor es im Hauptnetz bereitgestellt werden kann.
