# Modularität

Das Potenzial eines wirklich modularen DLT wird oft übersehen. Viele gehen davon aus, dass DLTs von Natur aus aktualisierbar sind, da sie Software sind. In der Praxis wird jedoch Software, die nicht modular aufgebaut ist, stagnieren. Die Flexibilität für zukünftige Upgrades ist entscheidend für den langfristigen Erfolg einer derart schnell fortschreitenden Technologie.

![03_hexagon-modularity](https://github.com/einfachiota/coordicide/raw/master/assets/03_hexagon-modularity.png)

Um dem IOTA-Protokoll diese Flexibilität zu geben und es in Zukunft für eine Vielzahl von Anwendungsfällen zu ermöglichen, erneuert die Coordicide-Lösung IOTA als modulares DLT. Wir haben mehrere Module entwickelt, die den Koordinator in der Konsensschicht der IOTA überflüssig machen.

Diese Module bieten verschiedene zusätzliche Vorteile, darunter:

- Verkürzte Endgültigkeitszeiten (innerhalb von Sekunden)
- Reduzierter Bedarf an "promotion" und "reattachment"
- Einführung eines Auto-Peering-Mechanismus
- Reduzierung der Nachrichtenmenge

Das Kernmodul von Coordicide ist ein verbesserter Konsensmechanismus: ein Abstimmungsschema, das den Algorithmus zur Auswahl von Tipps ergänzt, um die Dezentralisierung und Sicherheit zu maximieren. Wir haben auch ein System zur Zuordnung einer Identität zu jedem Knoten entwickelt. Durch Auto-Peering wird diese Identität zum Aufbau eines Small-World-Netzwerks und zur Steuerung der Transaktionsrate verwendet. Knoten stimmen dann ab, um Konflikte zu lösen, indem sie andere Knoten nach ihrem Ledgerstatus fragen.

In den folgenden Abschnitten werden die beiden vorgeschlagenen (sich nicht gegenseitig ausschließenden) Konsensimplementierungen erörtert: **Cellular Consensus** und [Fast Probabilistic Consensus](https://arxiv.org/pdf/1905.10895.pdf).


Wir verweisen interessierte Leser auch auf das [Coordicide White Paper](https://files.iota.org/papers/Coordicide_WP.pdf), das die hier vorgestellten Ideen weiter Beschreibt.

Was folgt, ist eine Karte der Grundbausteine für ein Post-Koordinator-IOTA-Netzwerk. Die IOTA Foundation ist derzeit dabei, einen Prototyp des Systems zu entwickeln und planen, Testnetze für einzelne Bausteine freizugeben, bevor die Komponenten zu einem einzigen Testnetz ohne Koordinatoren zusammengeführt werden. Es werden neue Simulationsergebnisse veröffentlicht, sobald sie verfügbar sind, und die IOTA Foundation freut sich darauf, mit der Community an diesen Testnetzen zu arbeiten.

### [Nächstes Kapitel](./04_bausteine.md)
### [Kapitel zurück](./02_iota_post-coordinator.md)
