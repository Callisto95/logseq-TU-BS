- Sei V ein K-Vektorraum
- eine Teilmenge $M\subseteq V$ heißt **Erzeugendensystem**, wenn $Span\space M=V$ gilt
	- d.h. für jedes $x\in V$ gibt es ein $n=n(x)\in\mathbb{N}$ und Vektoren $v_1,...,v_{n}\in M$ und Koeffizienten $\alpha_1,...,\alpha_{n}\in K$ mit $x=\sum_{j=1}^{n}\alpha_{j}v_{j}$
	- Problem: ein Vektor kann durch mehrere Ausdrücke dargestellt werden
	- Die Darstellung als Linearkombination liefert keine *eindeutigen* Koeffizienten
-
- Characterisierung von Basen
	- V Vektorraum, $B\subseteq V$
	- äquivalente Aussagen:
	- B ist eine Basis von V (B ist linear unabhängig und erzeugt V)
	  logseq.order-list-type:: number
	- B ist ein minimales Erzeugendensystem
	  logseq.order-list-type:: number
	- B ist eine maximale linear unabhängige Menge ($A\supsetneqq B$ => A ist nicht linear unabhängig)
	  logseq.order-list-type:: number
-
- Ergänzung linear unabhängiger Mengen
	- reference:: 5.10
	- V K-Vektorraum, $F\subseteq V$ linear unabhängig, $x\in V\setminus Span\space F$
	- $F\cup\lbrace x\rbrace$ ist linear unabhängig