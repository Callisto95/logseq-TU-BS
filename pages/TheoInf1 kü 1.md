exclude-from-graph-view:: true

-
- Verbände
  logseq.order-list-type:: number
	- $(x,y)\in\mathbb{N}$ und $n\in\mathbb{N}$
		- alle x=0 in relation mit allen anderen n
		- alle y=1 in relation mit allen anderen n
		- alle x=y=n
	- Hasse-Diagramm $(N,\leq)$, wobei Zahlen <= 9
	  logseq.order-list-type:: number
		- 0 zeigt auf alle {2,...,9} und die zeigen auf 1
	- $\bot=0,\top=1$
	  logseq.order-list-type:: number
	  id:: 671d0936-556c-4176-9930-7667575784d5
	- obere und untere Schranke
	  logseq.order-list-type:: number
		- $\bot\sqcup\top=1$
		- $\bot\sqcap\top=0$
		- $\top\sqcup5=\top=1$
		- $6\sqcap7=0$ keine Relation untereinander, aber beide gehen von 0 aus
		- $\bot\sqcup4=4$
		- $\sqcup\lbrace n\in\mathbb{N}:\text{x ist gerade}\rbrace=\sqcup\lbrace2n\in\mathbb{N}\rbrace=1$ 1 ist über allen Zahlen gestellt
	- Verband ist endlich mit beschränkter Höhe | Jede Kette hat endlich viele Elemente | Jede Kette hat maximal 3 Elemente
	  logseq.order-list-type:: number
	- unmöglich, da jede endliche Kette eine endliche Anzahl an Elementen hat. Somit existiert immer eine Schranke $n\in\mathbb{N}$
	  logseq.order-list-type:: number
		- ist möglich: bottom -> {{alle Zahlen mit einer Ziffer}, {alle Zahlen mit zwei Ziffern},...}
		-
- Verband mit natürlichen Zahlen
  logseq.order-list-type:: number
	- $\langle M,\preceq\rangle$ ist ein vollständiger Verband
	  logseq.order-list-type:: number
		- $\langle a_1,b_1\rang\preceq\langle a_2,b_2\rangle$ gdw. (genau dann, wenn) $a_1\geq a_2,b_1\geq b_2$
			- G1 ist *KLEINER* als G2, wenn die Inhalte *GRÖßER* sind
		-
		- Join, Meet existieren
			- jedes Element ist vergleichbar, sowie endlich
		-
		- Sei $a\in A,b\in B$ die größten Elemente in jeweils A und B, sodass $\forall a^{\prime}\in A:a\geq a^{\prime}$ und $\forall b^{\prime}\in B:b\geq b^{\prime}$
		- Das Tupel (a,b) ist somit $\forall a^{\prime}\in A,b^{\prime}\in B:(a,b)\preceq(a^{\prime},b^{\prime})$ bzw. $a\geq a^{\prime},b\geq b^{\prime}$
		- Damit ist (a,b) das Join von $(M,\preceq)$
		- das selbe gilt für das Meet, nur sind a,b kleiner gleich allen anderen Elementen
	- ist $\langle M,\preceq\rangle$ immer noch vollständig, wenn $M_1\subseteq\mathbb{N}$ unendlich ist
	  logseq.order-list-type:: number
		- Nein, da es kein Bottom gibt: $\forall(a,b)\in M:\exists(a^{\prime},b)\in M:(a^{\prime},b)\preceq(a,b)\Rightarrow a^{\prime}\geq a$
		-
- Produktverband
  logseq.order-list-type:: number
	- Produktverband ist ein vollständiger Verband
	  logseq.order-list-type:: number
		- $D_1,D_2$ sind vollständige, somit endliche, Verbände
		- $(D_1\times D_2,\preceq)$ ist somit auch endlich
		- Beweis für Meet und Join aus 2.a.
	- $(D_1\times D_2,\preceq)$ erfüllt ACC, wenn $(D_1,\preceq),(D_2,\preceq)$ ACC erfüllen
	  logseq.order-list-type:: number
		- $D_1,D_2$ sind endlich
		- $d_{m}\in D_1,d_{n}\in D_2$ als größte, stationäre Elemente von $D_1,D_2$
		- somit gibt es $(d_{11},d_{21})\preceq(d_{12},d_{22})\preceq...\preceq(d_{m},d_{n})$, was die ACC ist
- Jeder endliche Verband ist vollständig
  logseq.order-list-type:: number
	- vollständiger Verband: Join und Meet existieren
	- Verband $(D,\leq)$
	- sei g das größte Element in $(D,\leq)$
	- für g gilt also: $\forall d\in D:g\geq d$ (Die Eigenschaft einer oberen Schranke)
	- sei o die kleinste obere Schranke, sodass $o\leq o^{\prime}$ für alle oberen Schranken, gilt
	- durch die Anwendung der antisymmetrie: $g\leq o,o\leq g\Rightarrow o=g$
	- Das Join existiert
	- Das selbe gilt für das Meet
	- Es existieren somit ein Join und ein Meet, wodurch jeder endliche Verband ein vollständiger Verband ist
-
- ! partielle Ordnung muss noch nachgewiesen werden
- Beweise sind analog
-
- Kette in Hasse-Diagramm ist ein Pfad endlang eines gerichteten Pfades