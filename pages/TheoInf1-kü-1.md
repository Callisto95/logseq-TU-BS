exclude-from-graph-view:: true

-
- Verbände
  logseq.order-list-type:: number
	- Hasse-Diagramm $(N,\leq)$, wobei Zahlen <= 9
	  logseq.order-list-type:: number
	- $\bot=1,\top=9$
	  logseq.order-list-type:: number
	  id:: 671d0936-556c-4176-9930-7667575784d5
	- obere und untere Schranke
	  logseq.order-list-type:: number
		- $\bot\sqcup\top=9$
		- $\bot\sqcap\top=1$
		- $\top\sqcup5=\top=9$
		- $6\sqcap7=6$
		- $\bot\sqcup4=4$
		- $\sqcup\lbrace n\in\mathbb{N}:\text{x ist gerade}\rbrace=\sqcup\lbrace2n\in\mathbb{N}\rbrace=$ größte gerade Zahl in $\mathbb{N}$, da $\mathbb{N}$ unbegrenzt ist gibt es kein Join
	- Verband ist endlich mit beschränkter Höhe
	  logseq.order-list-type:: number
	- unmöglich, da jede endliche Kette eine endliche Anzahl an Elementen hat. Somit existiert immer eine Schranke $n\in\mathbb{N}$
	  logseq.order-list-type:: number
- Verband mit natürlichen Zahlen
  logseq.order-list-type:: number
	- $\langle M,\preceq\rangle$ ist ein vollständiger Verband
	  logseq.order-list-type:: number
		- $\langle a_1,b_1\rang\preceq\langle a_2,b_2\rangle$ gdw. (genau dann, wenn) $a_1\geq a_2,b_1\geq b_2$
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
		- Ja, da $M_2$, die andere "Vergleichsmenge", endlich ist. Somit existeren endliche viele Vergleiche und dadurch auch ein Join und Meet.
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
	- sei o das größte Element in $(D,\leq)$
	- für o gilt also: $\forall d\in D:o\geq d$ (Die Eigenschaft einer oberen Schranke)
	- $o\leq o^{\prime}$ für alle oberen Schranken
	-