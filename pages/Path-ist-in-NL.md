reference:: VL13

-
- Theorem
	- reference:: 9.17
	- Es sei $f:\mathbb{N}\rightarrow\mathbb{N}$ mit $\forall n:f\left(n\right)\geq\log n$
	- dann gilt $\text{coNSPACE}\left(O\left(f\right)\right)=\text{NSPACE}\left(O\left(f\right)\right)$
	- Beweis:
		- sei $L\in\text{NSPACE}$, also $L=L\left(M\right)$ für eine NTM M
		- zZ: Komplementproblem $\overline{L}$ durch eine $O\left(f\right)$-platzbeschränkte Maschine lösen lässt
		- Die Maschine M hat zu jeder Eignabe x eine initiale Konfiguration $c_0$
		- Es existiert eine eindeutige akzeptierende Konfiguration $c_{\text{acc}}$
		- Wir verändern M dazu so, dass sie beim Akzeptieren alle Arbeitsbänder löscht (bzw. mit BLANK überschreibt) und den Kopf auf dem read-only Band zur ersten Stelle der Eingabe bewegt
		- Betrachte zu M wieder den [[Konfigurationsgraph]] $G_{M}$
		- Eine Maschine löst $\overline{L}$ wie folgt:
			- Konstruiere Konfigurationsgraphen von M zur Eingabe x
			  logseq.order-list-type:: number
			- Wende Algorithmus für $\overline{\text{PATH}}$ auf diesen Graphen und Knoten $c_0$ und $c_{\text{acc}}$ an
			  logseq.order-list-type:: number
			- Akzeptiere, wenn es keinen Pfad gibt
		- Diese Maschine akzeptiert genau dann, wenn es keine akzeptierende Berechnung von M zur Eingabe x gibt, sie entscheidet also tatsächlich $\overline{L}$
	- Platzverbrauch
		- a) Konfigurationsgraph zu einer Eingabe der Länge n hat bei einer f-beschränkten Maschine Größe $2^{O\left(f\left(n\right)\right)}$
		- b) Der Algorithmus für $\overline{PATH}$ hat logaritmischen Platzverbrauch. Damit ist sein Platzverbrauch $O\left(\log2^{O\left(f\left(n\right)\right)}\right)=O\left(f\left(n\right)\right)$
		- Problematisch ist a), da zu viel Platz benötigt wird