# IOTA als skallierbares DLT

Ziel von IOTA ist es, ein DLT für das Internet der Dinge (IoT = Internet of Things) zu etablieren. Die folgenden Merkmale sind für diese Vision von grundlegender Bedeutung:

- **Skalierbarkeit.** Die Verarbeitung einer beträchtlichen Anzahl von Transaktionen pro Sekunde über ein großes Knotennetz mit schnellen Bestätigungszeiten.
- **Leichtgewichtigkeit.** Geräte mit geringem Stromverbrauch sollten in der Lage sein, direkt am Netzwerk teilzunehmen.
- **Gebührenfrei.** Das Senden von Transaktionen sollte keine Zahlung von Netzwerkgebühren erfordern.

Herkömmliche DLTs weisen begrenzende Faktoren auf, die sie zur Erreichung des IOTA-Ziels ungeeignet machen.

## 1. Die Blockchain-Datenstruktur

Die eigen Beschränkung der Geschwindigkeit von Blockchain-Netzwerken wird allgemein als "Blockchain-Engpass" ("bottleneck") bezeichnet. Bei der Blockchain gibt es nur eine Stelle, an die neue Transaktionen angefügt werden können - das Ende der Kette. Die daraus resultierenden negativen Auswirkungen auf den Netzwerkdurchsatz werden in dieser einfachen Grafik dargestellt:

![01_blockchain_bottleneck](https://github.com/einfachiota/coordicide/raw/master/assets/01_blockchain_bottleneck.gif)

Im Gegensatz dazu ist die Kerndatenstruktur in IOTA hochgradig skalierbar. Dies wird mit einer einfachen Regel ermöglicht: Jede Transaktion referenziert und genehmigt zwei bestehende Transaktionen. Diese Regel definiert die zugrunde liegende Datenstruktur von IOTA - dem Tangle -, das mathematisch als gerichteter azyklischer Graph (DAG) bezeichnet wird.

DAGs sind nicht auf eine einzige Stelle zum Anhängen neuer Transaktionen beschränkt, sondern bieten mehrere Stellen, an denen Transaktionen angehängt werden können. Benutzer können weiterhin neue Transaktionen an verschiedene Teile des Tangle anhängen, ohne auf die Bestätigung durch andere Transaktionen zu warten:

![01_tangle_bottleneck](https://github.com/einfachiota/coordicide/raw/master/assets/01_tangle_bottleneck.gif)

## 2. Der Konsensmechanismus.

Bei der Blockchain teilt der Nakamoto-Konsens das Netzwerk in Miner und Benutzer auf. Miner verbrauchen viel Rechenleistung, um den Proof-of-Work (PoW) durchzuführen, der zum Verketten der Blöcke erforderlich ist. Miner erhalten Anreize durch die Gebühren, die die Nutzer zu zahlen bereit sind, damit ihre Transaktion in einem Block enthalten ist. Diese gebührenpflichtige Anreizstruktur wäre ein erhebliches Hindernis in einer Maschine-zu-Maschine-Wirtschaft, in der die Micropayment-Werte zwischen Maschinen unter den anfallenden Gebühren liegen können.

In IOTA gibt es keinen Unterschied zwischen Minern und Nutzern. Alle Knoten (Nodes)können am Konsens teilnehmen. Dies bedeutet, dass ein IOTA-Knoten eine völlig andere Rolle spielt als ein Bitcoin-Miner. IOTA-Knoten führen nur grundlegende Operationen aus, die nicht viel Rechenleistung erfordern (z. B. Speichern des Ledgers, Validieren von Transaktionen). Benutzer können mit minimalen Kosten einen Knoten einrichten und aktiv am Netzwerkkonsens teilnehmen, wodurch die Sicherheit des Netzwerks gestärkt wird.

Die Definition einer Konsensschicht, die beschreibt, wie sich Knoten darauf einigen, welche Transaktionen vertrauenswürdig sind, ist das Kernstück von IOTA. In der aktuellen IOTA-Implementierung vertrauen Knoten Transaktionen, die von Meilensteinen referenziert und genehmigt werden, die vom Koordinator ausgestellt wurden. Die Verwendung dieses zentralen „Finality-Geräts“ war notwendig, um die Sicherheit in den Kinderschuhen des Netzwerks zu gewährleisten.

![01_milestones](https://github.com/einfachiota/coordicide/raw/master/assets/01_milestones.gif)

Die Lösung für Coordicide stellt sicher, dass das Netzwerk nicht beeinträchtigt wird, gleichzeitig werden Dezentralisierung und Sicherheit gewährleistet und eine beispiellose Skalierbarkeit gefördert.