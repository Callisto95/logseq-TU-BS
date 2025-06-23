reference:: 9.4

- sei $x_0,x_1,...$ eine abzählbar unendliche Menge an Aussagenvariablen
- Ein *Literal* ist von der Form $x_{i}$ (positiv), $\neg x_{i}$ (negativ)
- Eine *Klausel* C ist eine Disjunktion von Literalen (also $c=\bigvee L_{k}$)
- Eine aussagenlogische Formel in KNF (auch CNF) ist eine Konjunktion von Klauseln
	- $F=\bigvee C_{n}$
	- z.B. $\left(\neg x\lor y\right)\land\left(\neg y\lor z\right)\land\left(x\lor\neg z\right)\land\left(z\lor y\right)$
		- setze x=1,y=1,z=1