reference:: 9.4

- sei $x_0,x_1,...$ eine abzählbar unendliche Menge an Aussagenvariablen
- Ein *Literal* ist von der Form $x_{i}$ (positiv), $\neg x_{i}$ (negativ)
- Eine *Klausel* C ist eine Disjunktion von Literalen (also $c=\bigvee L_{k}$)
- Eine aussagenlogische Formel in KNF (auch CNF) ist eine Konjunktion von Klauseln
	- $F=\bigvee C_{n}$
	- z.B. $\left(\neg x\lor y\right)\land\left(\neg y\lor z\right)\land\left(x\lor\neg z\right)\land\left(z\lor y\right)$
		- setze x=1,y=1,z=1
-
- Problem: SAT
- Gegeben: eine Formel F in KNF
- Frage: Gibt es eine Belegung $\varphi$ mit $\varphi\left(F\right)=1$
- Variation: k-Sat
	- Änderung: Gegeben: eine Formel in k-KNF
-
- Eine Formel ist in k-KNF, wenn sie in KNF ist und jede Klausel höchstenz k Literale besitzt
-
- Theorem
	- reference:: 9.18
	- 2SAT ist NL-vollständig
	- z.Z.:
		- "Membership": 2SAT$\in$NL
		- "Hardness": 2SAT ist NL-schwer (oder ist coNL-schwer)
-
- Lemma: **2SAT ist in coNL**
	- reference:: 9.19
	- aus $z\lor y:\neg z\Rightarrow y,\neg y\Rightarrow z$
	- aus $\neg y\lor z:y\Rightarrow z,\neg z\Rightarrow\neg y$
	- aus $\neg x\lor y:x\Rightarrow y,\neg y\Rightarrow\neg x$
	- aus $x\lor\neg z:z\Rightarrow x,\neg x\Rightarrow\neg z$
	- ![Untitled Diagram.drawio.png](../assets/Untitled_Diagram.drawio_1750679568669_0.png){:height 147, :width 307}
	- aber: $F=\left(x\right)=\left(x\lor x\right)$
		- also $\neg x\Rightarrow x$
	- Für eine gegebene 2-KNF F konstruieren wie einen Graph $G_{F}=\left(V_{F},E_{F}\right)$ wie folgt:
		- $V_{F}=\left\lbrace x,\neg x;x\text{ ist eine Variable in F}\right\rbrace$
		- Für jede Klausel $\left(\alpha\lor\beta\right)$ erhalten wir Kanten $\left(\neg\alpha,\beta\right),\left(\neg\beta,\alpha\right)$
		- Für jede Klausel $\left(\alpha\right)$ erhalten wie die Kante $\left(\neg\alpha,\alpha\right)$
-
- Lemma
	- reference:: 9.21
	- Eine 2-KNF F ist genau dann unerfüllbar, wenn es eine Variable x gibt, für welche in $G_{F}$ ein Pfad von x nach $\neg x$ und ein Pfad von x nach $\neg x$ existieren
	- Beweis
		- "<="
			- Angenommen die beiden Pfade existieren, aber es gibt eine erfüllbare Belegung $\varphi\left(F\right)=1$, und o.B.d.A.: $\varphi\left(x\right)=1$
			- Damit ist $\varphi\left(\neg x\right)=0$
			- Da es einen Pfad von x nach $\neg x$ gibt, existiert Kante $\left(L,L^{\prime}\right)$ auf dem Pfad mit $\varphi\left(L\right)=1,\varphi\left(L^{\prime}\right)=0$
			- Diese Kante entspricht der Klausel $\neg L\lor L^{\prime}$, welche damit zu 0 evaluiert wird, d.h. $\varphi\left(F\right)=0$
			- => Wiederspruch dazu, dass $\varphi$ F erfüllt
		- "=>"
			- Angenommen einer der beide Pfade existiert nicht
			- Konstruktion einer erfüllenden Belegung durch
				- while $\exists$Literal ohne Wahrheitswert do
					- wähle Literal L, sodass kein Pfad von L nach $\neg L$ existiert
					- $\forall$Literale L', die von L erreichbar sind:
						- setze $\varphi\left(L^{\prime}\right)=1$
					- $\forall$Literale L', die $\neg L$ erreichen
						- setze $\varphi\left(L^{\prime}\right)=0$
			- Wir müssen begründen, dass die resultierende Belegung $\varphi$ eine wohldefinierte Belegung ist
				- Jedem Literal wird ein Wahrheitswert zugewiesen
					- sei L ein Literal ohne Wahrheitswert, dann ist auch L' nicht belegt
					- Falls wie L nicht auswählen können, dann können wir L' auswählen
				- Die Belegung ist wohldefiniert
					- Angenommen es gibt ein Literal L', sodass L' und $\neg L^{\prime}$ den selben Wert haben
					- Beide Literale erhalten im selben Durchlauf ihren Wert (z.B. wenn L gewählt wurde)
					- Dann gibt es entweder Pfade von L nach L' und $\neg L^{\prime}$ oder L ist von L' und $\neg L^{\prime}$ erreichbar
					- Es gelte $L\rightarrow^{\ast}L^{\prime}$ und $L\rightarrow^{\ast}\neg L^{\prime}$
					- Aus Symmetriegründen existiert $\neg L^{\prime}\rightarrow^{\ast}\neg L$ und $L^{\prime}\rightarrow^{\ast}\neg L$, also $L\rightarrow^{\ast}L^{\prime}\rightarrow\neg L$
					- Wiederspruch durch Wahl von L
				- $\varphi$ erfüllt F
					- Wenn L ein Literal ist, welches auf 1 gesetzt wird, dann gibt es kein von L aus erreichbates Literal, welches auf 0 gestzt wurde
					- => Alle Implikationen im Graphen sind also erfüllt
-
- Der Folgende Algorithmus löst $\overline{2\text{SAT}}$
	- Eingabe: 2KNF F
	- Ausgabe: 1, falls F unerfüllbar ist
	- Konstruiere $G_{F}$
	  logseq.order-list-type:: number
	- for Variable x in F do
	  logseq.order-list-type:: number
		- if $G_{F}\#x\#\neg x\in\text{PATH}$ und $G_{F}\#\neg x\#x\in\text{PATH}$ then
			- return true
	- return false
	  logseq.order-list-type:: number
	- ---
	- in LOGSPACE?
		- Graph muss "On-The-Fly" erstellt werden
-
- Lemma: **2SAT ist coNL-schwer**
	- reference:: 9.23
	- Skizze (siehe Skript): $\overline{ACYCLICPATH}\leq_{m}^{\log}$2SAT
-