- ein Graph is 2-färbbar, wenn es eine Funktion $c:V\rightarrow\left\lbrace0,1\right\rbrace$ gibt, sodass $\forall e=\left\lbrace u,v\right\rbrace\in E$ gilt $c\left(u\right)\neq c\left(v\right)$
-
- Problem: 2-COL
	- Gegeben: Graph G
	- Frage: ist G 2-färbbar?
	- Lemma: Ein Graph G ist 2-färbbar gdw. in G kein Kreis ungerader Länge existiert
- Problem "Odd-Cycle":
	- Gegeben: Graph G
	- Frage: Existiert in G ein Kreis ungerader Länge?
-
- => $2\text{-COL}\leq_{m}^{\log}\overline{\text{ODD-CYCLE}}$, $\overline{\text{ODD-CYCLE}}\leq_{m}^{\log}\text{2-COL}$
- Beweis: Lemma
	- "=>"
		- Annahme: es exisitert ein Kreis ungerader Länge
		- sei dieser $\left(\ast v_{k}\right)$ mit $k\bmod2=1$
		- da jeder gerade Index nur zu ungeraden Indizes benachbart sind, muss $c\left(v_{i}\right)\neq c\left(v_{j}\right)$ sein, mit $i\bmod2=0,j\bmod2=1$
		- => gerade Indezies erhalten Farbe 0, damit müssen alle ungeraden Indizes die Farbe 1 erhalten
		- => $c\left(v_1\right)=c\left(v_{k}\right)$ -> nicht 2-färbbar
	- "<="
		- Wenn es keinen ungeraden Kreis gibt, wollen wir eine 2-färbung berechnen
			- Wähle bel $s\in V$
			  logseq.order-list-type:: number
			- bestimme BFS-Baum von G mit Start s
			  logseq.order-list-type:: number
				- -> man erhält Distanzen d(v) zu s
			- setze $c\left(v\right)\coloneqq d\left(v\right)\bmod2$
			  logseq.order-list-type:: number
		- Angenommen diese Färbung ist nicht gültig
		- Dann exisitieren $u,v\in V$ mit $c\left(u\right)=c\left(v\right)$ und $\left\lbrace u,v\right\rbrace\in E$
		- nach Konstruktion ist $d\left(u\right)=d\left(v\right)$
		- Dann ist $s\rightarrow^{\ast}v\rightarrow w\rightarrow^{\ast}s$ ein Kreis der Länge $d\left(u\right)+d\left(v\right)+1=2\cdot d\left(u\right)+1$, also ungerade -> Wiederspruch
		- => Färbung ist gültig
-
- Problem: Undirected-s-t-Path (USTCON)
	- Gegeben: Ungerichteter Graph G=(V,E), Knoten $s,t\in V$
	- Frage: Existiert ein Pfad von s nach t in G?
	- Man kann zeigen: USTCON $\in$ L
	- -> gilt Odd-Cycle $\leq_{m}^{\log}$ USTCON?
-
- Reduktion Odd-Cycle $\leq_{m}^{\log}$ USTCON:
	- Erstelle Graphen $G^{\prime}=\left(V^{\prime},E^{\prime}\right)$ mit $V^{\prime}=V\times\left\lbrace0,1\right\rbrace$
	- für jede Kante $\left\lbrace u,v\right\rbrace\in E$ füge Kanten $\left\lbrace\left(u,0\right),\left(u,1\right)\right\rbrace$ und $\left\lbrace\left(v,0\right),\left(v,1\right)\right\rbrace$ zu E hinzu
	- Behauptung: G besitzt genau dann einen ungeraden Kreis C mit $s\in L$, wenn $G^{\prime}$ einen (s,0)-(s,1)-Pfad besitzt
	- Beweis
		- "=>"
			- sei $\left(s,v_0,\ast v_{k}\right)$ mit $k\bmod2=1$ ein ungerader Kreis
			- in G' entspricht dies der Folge $\left(s,0\right),\left(v_0,1\right),\left(v_1,0\right),\left(v_2,1\right),...,\left(v_{k},0\right),\left(s,1\right)$
			- -> Es existiert ein (s,0)-(s,1)-Pfad in G'
		- "<="
			- sei P=((s,0),...,(s,1)) ein (s,0)-(s,1)-Pfad in G'
			- Dann besitzt P gerade viele Knoten
			- Da (s,0)$\equiv$(s,1) in G ist, muss der erhaltene Kreis $\left(s,v_0,\ast v_{k}\right)$ ungerade sein
			- nun muss s nicht auf einem ungeraden Kreis liegen
			- Sei $G_{v}^{\prime}$ der konstruierte Graph wie beschrieben
			- Erstelle $G_{v}^{\prime}$ für $v\in V$
			- Füge neue Knoten s,t hinzu, sowie Knoten s->(v,0) in $G_{v}^{\prime}$ sowie (v,1)->t mit $\left(v,1\right)\in G_{v}^{\prime}$
			- Lemma: G enthält einen ungeraden Kreis <=> neuer Graph einen s-t-Pfad besitzt