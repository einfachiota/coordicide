# MODUL 1  - NODE IDENTITIES UND MANA

In einem Netzwerk ohne den Koordinator müssen wir in der Lage sein, Transaktionen oder andere Nachrichten zuverlässig dem Knoten zuzuordnen, der sie ausgegeben hat. Damit Knoten abstimmen können, müssen wir sie (und ihre Stimmen) identifizieren können. Jeder Knoten generiert daher eine eindeutige Kennung, mit der er Nachrichten signiert oder Stimmen abgibt und so die Authentizität sicherstellt.

Die Abhängigkeit von Knotenidentitäten macht verteilte Systeme jedoch anfällig für Sybil-Angriffe. Ein Schutz gegen solche Angriffe besteht darin, die Anzahl der Stimmen, die ein Knoten abgeben kann, mit einer knappen Ressource zu verknüpfen, z. B. Hashing-Leistung in PoW oder dem einfrieren von Werten in Proof-of-Stake (PoS).

Im Gegensatz zu PoW-basierten DLTs weist PoS keine Skalierbarkeitsprobleme auf. In einer Umgebung mit "Gewinnen mit der längsten Kette" ist PoS jedoch anfällig für bestimmte Angriffe, z. B. für das "Nichts-steht-auf-dem-Spiel-Problem" (“nothing-at-stake problem” ), bei dem Parteien gleichzeitig für zwei in Konflikt stehende Ketten stimmen können, ohne Ressourcen zu riskieren oder zu investieren oder auch „Fernangriffe“, bei denen große Stakeholder eine längere Kette im Verborgenen halten und später ausstrahlen können. Diese beiden Angriffsvektoren machen PoS in Netzwerken mit den längsten Gewinnketten unerwünscht.

Da unsere Coordicide-Lösung nicht auf der Regel der längsten Kettengewinne beruht, ist unser Sybil-Schutzmechanismus von diesen Problemen nicht betroffen.

Wir schlagen ein Reputationssystem vor, das wir Mana nennen:

- Durch das Versenden von IOTA in einer Werttransaktion beweisen Benutzer das Eigentum an dem übertragenen IOTA-Betrag.
- Benutzer können Werttransaktionen mit einem Knoten ihrer Wahl verknüpfen, indem sie der Transaktionssignatur eine Knoten-ID hinzufügen. In der Praxis wird dies höchstwahrscheinlich derselbe Knoten sein, der zum Ausgeben der Transaktion verwendet wird.
- Die Transaktion führt zu einer Manaverschiebung von dem Knoten, dem sie zuvor zu dem in dieser Transaktion angegebenen Knoten zugewiesen wurde. Dies erhöht das Gesamtmana des ausgewählten Knotens.

![04_1_mana](https://github.com/einfachiota/coordicide/raw/master/assets/04_1_mana.gif)


Das Manasystem kombiniert die Vorteile eines fondsbasierten Sybil-Schutzmechanismus mit denen eines Reputationssystems. Mana wird nicht nur einem Knoten gutgeschrieben, indem IOTA-Token an den Knotenbesitzer übertragen werden. Sie erhalten es auch, indem Sie der Community einen guten Service bieten und gültige Transaktionen an das Netzwerk weitergeben. Der Betrag des insgesamt gutgeschriebenen Manas - als Maß für das Vertrauen oder den Ruf - kann verwendet werden, um „gute“ Akteure auf andere Weise weiter zu belohnen (z. B. in den Modulen zur Ratenkontrolle oder Abstimmung).

Mana beruht auf der Vorstellung, dass es schwierig ist, Ansehen zu erlangen, aber leicht zu verlieren. Ein Schlüsselaspekt jedes Reputationssystems ist die Fähigkeit, schlechte Mitspieler zu bestrafen, indem sie zuvor gewährte Reputation widerrufen. In IOTA ist dies so einfach wie das erneute Zuweisen Ihres gewährten Manas zu einem anderen Knoten, wenn festgestellt wird, dass sich Ihr derzeit bevorzugter Knoten „schlecht benimmt“ (z. B. das Weitergeben ungültiger Transaktionen).

Ein entscheidender Vorteil von Mana ist schließlich, dass im Gegensatz zu anderen Sybil-Schutzmechanismen, bei denen die Knoten-ID mit dem privaten Schlüssel des Eigentümers verknüpft ist und Benutzer zur Teilnahme an komplexen und potenziell riskanten Einsätzen gezwungen werden. Das Manasystem sorgt dafür,dass ein großer Teil der Mittel für die Zuweisung von Ruf verwendet wird.

### [Nächstes Kapitel](./04_module_2)
### [Kapitel zurück](./04_bausteine)