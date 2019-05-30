# MODUL 2  - SICHERES AUTO-PEERING

In Peer-to-Peer-Netzwerken wie IOTA sind die Nachbarn eines Knotens die einzige Informationsquelle. Jeder Peering-Mechanismus muss sich daher darauf konzentrieren, eine Verbindung zu einer gesunden Anzahl von ehrlichen Nachbarn herzustellen, d. H. Knoten, die nicht versuchen, das Netzwerk zu schädigen.

Wir führen einen Auto-Peering-Mechanismus ein, bei dem jeder Knoten seine eigenen Kriterien für die Auswahl potenzieller Nachbarn hat. Ein Angreifer kann die Entscheidungen eines Knotens im Peer-Auswahlprozess nicht beeinflussen. Daher ist die bestimmte „Sicht“ eines Knotens auf das Netzwerk sowohl lokal als auch unvorhersehbar. Dies dient dem Schutz vor Angriffen von außen (z. B. Eclipse-Angriffen) und macht es Angreifern praktisch unmöglich, bestimmte Knoten im Peering-Prozess anzugreifen, während sichergestellt wird, dass die Knoten immer mindestens eine bestimmte Anzahl ehrlicher Nachbarn haben.

![04_2_auto_peering](https://github.com/einfachiota/coordicide/raw/master/assets/04_2_auto_peering.gif)

Darüber hinaus wird der Auto-Peering-Mechanismus versuchen, ein Small-World-Netzwerk zu erstellen, in dem Knoten von jedem anderen Knoten über eine kleine Anzahl von Zwischenschritten erreicht werden können. Diese Eigenschaft beschleunigt das Erziellen eines Konsens erheblich.