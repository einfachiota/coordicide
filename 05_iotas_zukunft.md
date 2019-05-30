# IOTA's Zukunft

Bisher haben wir die direkten Auswirkungen von Coordicide auf das IOTA-Netzwerk und die zugrunde liegende Technologie erörtert. Das Coordicide-Projekt ermöglicht jedoch weit mehr als nur ein „besseres“ Netzwerk.

Es gibt indirekte Implikationen, die ebenso faszinierend sind, aber möglicherweise nicht sofort offensichtlich sind. Obwohl diese Website nicht den Umfang hat, diese Auswirkungen ausführlich zu behandeln, möchten wir dennoch einige erste Diskussionen über einige der wichtigsten Funktionen aufzeigen.

## Zuverlässige Zeitstempel
![05_future1](https://github.com/einfachiota/coordicide/raw/master/assets/05_future1.png)

Anstatt direkt über das Schicksal von Transaktionen abzustimmen, können wir auch über die Glaubwürdigkeit von Zeitstempeln abstimmen. Hier bedeutet "glaubwürdig", dass die Differenz zwischen dem ausstellenden Zeitstempel einer Transaktion und ihrer Ankunftszeit an den Knoten einen bestimmten Schwellenwert nicht überschreitet.

Ob eine Transaktion beliebt ist, kann dann lokal abgeleitet werden, d. H. Indem die früheste Transaktion mit einem glaubwürdigen Zeitstempel bei Vorliegen von Konflikten bevorzugt wird. Dies hat mehrere Vorteile:

- Sogar Geräte, die nicht vollständig über den Status des Ledgers informiert sind, können am Abstimmungsprozess teilnehmen. Dies ist äußerst vorteilhaft für die Synchronisierung von Knoten und der IoT-Umgebung, in der Geräte über unzuverlässige Verbindungen verfügen.

- Da das Netzwerk einen Konsens darüber erzielen kann, welche Transaktionen glaubwürdige Zeitstempel enthalten, können wir anfangen, auf Zeitstempelwerte zu vertrauen und ein vollständig geordneten Tangle aufzubauen. Wenn zwei Transaktionen den gleichen Zeitstempel tragen, sortieren wir sie einfach nach ihrem Transaktions-Hash.

Die Unfähigkeit, einen geordnete Reihenfolge zu erstellen, war einer der größten Nachteile von DLTs auf DAG-Basis in Bezug auf „intelligente Verträge“.

## mehrere Tangles (Domänen)
![05_future2](https://github.com/einfachiota/coordicide/raw/master/assets/05_future2.png)

Ohne den Koordinator ist es möglich, dass mehrere Tangles gleichzeitig als separate Domänen existieren. Jede Domäne kann eine andere Logik für die von ihr verarbeiteten Transaktionen implementieren (über verschiedene IXI-Module) und den enthaltenen Token eine andere Bedeutung zuordnen. Auch wenn diese Domänen nicht unbedingt dieselben Regeln verwenden, ist es dennoch möglich, dass Transaktionen von einer Domäne auf Daten von einer anderen Domäne verweisen.

Auf diese Weise können wir äußerst komplexe Anwendungsfälle mit sehr einfachen Bausteinen modellieren. Beispielsweise können Ressourcentoken in einer Domäne das Recht darstellen, auf bestimmte Ressourcen zuzugreifen, wohingegen Asset-Token in einer anderen Domäne den Besitz eines Anteils eines bestimmten Assets darstellen können.

Der modulare Ansatz bietet nicht nur viel Flexibilität für IOTA, sondern ermöglicht auch die Aufteilung der Netzwerkaktivität in separate Domänen und erhöht damit die Skalierbarkeit von IOTA. Beispielsweise könnte ein "Nur-Daten" -Tangle, das nur Datentransaktionen enthält, von einem Tangle getrennt werden, das nur Werttransaktionen enthält. Da bei Datentransaktionen niemals Konflikte auftreten können, können Transaktionen in diesem Tangle ohne Einbeziehung eines Konsensmechanismus sofort bestätigt werden. Dies würde eine Vielzahl von IoT-Anwendungsfällen ermöglichen, die von unveränderlichen Daten abhängen.

## Unterschiedliche Datenstrukturen für jede Domain
![05_future3](https://github.com/einfachiota/coordicide/raw/master/assets/05_future3.png)

Da der Tangle die allgemeinste Form der DAG ist und Bundles 1 auf n andere Transaktionen verweisen können, können jetzt ganz andere Datenstrukturen erstellt werden, die auf die spezifischen Anforderungen eines Anwendungsfalls zugeschnitten sind. Durch Implementieren eines anderen Tippauswahlalgorithmus kann eine blockchainartige Struktur erstellt werden, bei der Stamm und Zweig einer Transaktion immer auf die vorherige Transaktion verweisen. In ähnlicher Weise könnten Strukturen wie „Blockgitter“ leicht mit einem anderen Algorithmus für die Tippauswahl emuliert werden. Den Möglichkeiten sind wirklich keine Grenzen gesetzt. Der modulare Ansatz garantiert die ultimative Freiheit des Protokolls.

## Zusätzliche Regeln, die im Signaturnachrichtenfragment codiert sind

Da jede Transaktion ein „Signaturnachrichtenfragment“ (“signature message fragment”) enthält, das beliebige Daten enthalten kann, können komplexere Verhaltensweisen codiert werden (z. B. bestimmte Bedingungen für die Anwendung einer Transaktion oder automatisch ausgelöste Nebenwirkungen). Diese können dann analysiert und von den Knoten dieser bestimmten Domäne angewendet werden.

### [Nächstes Kapitel](./06_zusammenfassung)
### [Kapitel zurück](./04_module_5_3)

