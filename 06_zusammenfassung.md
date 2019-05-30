# Zusammenfassung

Ziel dieser Website war es, die Konzepte von Coordicide und seinen verschiedenen Modulen vorzustellen. Die folgende Liste fasst die Auswirkungen dieser Module zusammen und erläutert die Eigenschaften, die ein koordinatorenloses Netzwerk in die Tabelle einbringt:

## VOLLSTÄNDIGE DEZENTRALISIERUNG
![06_decentralizaton](https://github.com/einfachiota/coordicide/raw/master/assets/06_decentralizaton.png)
Ohne den Koordinator hat keine Einheit eine besondere Rolle im Netzwerk. Absolute Klarheit: Sobald der Koordinator abgeschaltet ist, kann er von der IOTA-Stiftung nicht mehr neu gestartet werden.

## PERMISSIONLESS NETZWERK
![06_permissionless](https://github.com/einfachiota/coordicide/raw/master/assets/06_permissionless.png)
Jeder kann sich jederzeit dem Netzwerk anschließen. Wenn andere DLTs ihre Knotennummern begrenzen oder sogar einen zulässigen Ansatz für die Skalierbarkeit einführen müssen, umfasst unser Ansatz zusätzliche Knoten. Eine größere Anzahl ehrlicher Knoten verbessert die Sicherheit des Netzwerks, indem der Anteil ehrlicher Stimmen erhöht wird.

## ENDGÜLTIGKEIT INNERHALB VON SEKUNDEN
![06_finality](https://github.com/einfachiota/coordicide/raw/master/assets/06_finality.png)
Durch den Abstimmungsprozess kann das Netzwerk sehr schnell Entscheidungen über Transaktionen treffen und abschließen, ohne auf mehrere zusätzliche genehmigende Transaktionen warten zu müssen, um die Sicherheit zu erhöhen. Darüber hinaus kann das Netzwerk eine „wahre Finalität“ erreichen (eher deterministisch als probabilistisch), da ein Angreifer mit unbegrenzter Hashing-Fähigkeit den Status des Ledgers nicht „umkehren“ kann.

## ZUVERLÄSSIGES TIMESTAMPING / VOLLSTÄNDIG GEORDNETER TANGLE
![06_reliable](https://github.com/einfachiota/coordicide/raw/master/assets/06_reliable.png)
Der Aussteller der Transaktion (Knoten / Benutzer) legt zum Zeitpunkt der Ausstellung einen Zeitstempel fest. Das Erreichen eines Konsenses über die Glaubwürdigkeit von Zeitstempeln ermöglicht es uns, ein vollständig geordneten Tangle zu erstellen - ein großer Schritt in Richtung intelligenter Verträge ("smart contracts") (siehe Abschnitt "Zukunft" von IOTA).

## SKALIERBARKEIT IN DER NODE ANZAHL UND TRANSKATION VERABREITUNGSMENGE
![06_scalability](https://github.com/einfachiota/coordicide/raw/master/assets/06_scalability.png)
Es gibt keine protokollbezogenen Engpässe. Die Skalierbarkeit ist nur durch Hardware und die Gesetze der Physik begrenzt. Die Entfernung des Koordinators als eine Einheit, die alle Transaktionen verarbeitet und überprüft, bildet die Grundlage für einen dynamischen Sharding-Prozess, der als "wirtschaftliches Clustering" ("economic clustering") bezeichnet wird und eine „echte“ unbegrenzte Skalierbarkeit ermöglicht.

## ADAPTIVE RATE CONTROL ALGORITHM
![06_adaptive_rate](https://github.com/einfachiota/coordicide/raw/master/assets/06_adaptive_rate.png)
Ein Algorithmus zur adaptiven Ratensteuerung, der auf Knotenbasis arbeitet, macht es Angreifern unmöglich, das Netzwerk mit ungesundem Spam zu überfluten, während ehrliche Knoten normal funktionieren.

## ERHÖHTE ZUVERLÄSSIGKEIT (EINE REDUZIERTE NOTWENDIGKEIT FÜR REATTACHMENTS UND PROMOTIONS)
![06_reliable](https://github.com/einfachiota/coordicide/raw/master/assets/06_reliable.png)
Das Bestimmen des bevorzugten Teils des Tangles durch Abstimmung ermöglicht die Implementierung unterschiedlicher Tippauswahlstrategien, durch die die meisten (wenn nicht alle) ehrlichen Transaktionen aufgegriffen werden. Dies reduziert den Bedarf an reattachments und promotions.

## SICHERHEIT
![06_security](https://github.com/einfachiota/coordicide/raw/master/assets/06_security.png)
Der neuartige Sybil-Schutzmechanismus führt zu extrem viel Mana und sichert zusammen mit den zusätzlichen Sicherheitsebenen des Abstimmungsmechanismus das Netzwerk auch bei Anwesenheit einer großen Anzahl von Gegnern.

## CLEVERES UND ROBUSTES AUTO-PEERING
![06_auto-peering](https://github.com/einfachiota/coordicide/raw/master/assets/06_auto-peering.png)
Das Entfernen des manuellen Peerings reduziert den Wartungsaufwand für die Knotenbetreiber und macht das Netzwerk robuster.

## GEBÜHRENLOSE TRANSAKTIONEN
![06_feeless](https://github.com/einfachiota/coordicide/raw/master/assets/06_feeless.png)
Die Abwesenheit von Minern macht IOTA-Transaktionen völlig kostenlos und ermöglicht Mikrozahlungen sowohl für den Menschen als auch für die Machine-to-Machine-Wirtschaft.

## Quantum Robustheit
![06_quantum](https://github.com/einfachiota/coordicide/raw/master/assets/06_quantum.png)
Das einmalige Signaturschema von Winternitz macht IOTA robust gegenüber Quantencomputern, wenn sie allgemein verfügbar werden.

## DATENTRANSAKTIONEN
![06_transactions](https://github.com/einfachiota/coordicide/raw/master/assets/06_transactions.png)
Datentransaktionen ermöglichen Anwendungsfälle der Technologie in vielen Bereichen.

## LOCAL SNAPSHOTS
![06_local](https://github.com/einfachiota/coordicide/raw/master/assets/06_local.png)
Mit lokalen Snapshots (Local snapshots) können Knoten nur einen Teil des Ledger-Verlaufs speichern, sodass Knoten mit begrenzten Hardwareressourcen am Netzwerk teilnehmen können.

## GERECHTIGKEIT
![06_fairness](https://github.com/einfachiota/coordicide/raw/master/assets/06_fairness.png)
Alle Transaktionen werden gleich behandelt. Es gibt keine Möglichkeit, eine Prämie (z. B. durch erhöhte Gebühren) zu zahlen, um eine höhere Priorität bei der Verarbeitung durch das Netzwerk zu erhalten.

## LEICHTGEWICHTIG
![06_lightweight](https://github.com/einfachiota/coordicide/raw/master/assets/06_lightweight.png)
Geräte mit geringem Stromverbrauch können Transaktionen ausführen und am Konsens teilnehmen.

## MODULARITÄT
![06_modularity](https://github.com/einfachiota/coordicide/raw/master/assets/06_modularity.png)
Durch den modularen Aufbau können die Bauteile des Protokolls unabhängig voneinander entwickelt werden. Der mehrschichtige Ansatz ermöglicht eine Erweiterung des Basisprotokolls auf ähnliche Weise wie das Internetprotokoll.

## GEMEINNÜTZIGE STIFTUNG
![06_governance](https://github.com/einfachiota/coordicide/raw/master/assets/06_governance.png)
Die gemeinnützige Organisation hinter IOTA optimiert die Akzeptanz und zukünftige Entwicklung des Netzwerks. Die Abwesenheit von Minern ermöglicht die Implementierung neuer Funktionen ohne Interessenkollusion.

## OPEN SOURCE
![06_open_source](https://github.com/einfachiota/coordicide/raw/master/assets/06_open_source.png)
Die Technologie ist kostenlos, Open Source und jeder kann darauf Lösungen aufbauen.


![team](https://github.com/einfachiota/coordicide/raw/master/assets/team.png)


Wir hoffen, dass du nach dem Lesen dieser Website und der technischen Dokumente ein besseres Verständnis für die bevorstehenden Herausforderungen hast, aber auch unsere Begeisterung für unseren weiteren Weg teilst.

Coordicide Team - Mai 2019