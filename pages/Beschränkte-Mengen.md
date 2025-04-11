- **oben beschränkt**
  collapsed:: true
	- $B\subseteq\mathbb{R}$ heißt nach oben beschränkt, wenn es eine obere Schranke $s_{o}\in\mathbb{R}$ existiert
	- es gilt $\forall b\in B:b\leq s_{o}$
		- genau: $\exists s_{o}\in\mathbb{R}:\forall b\in B:b\leq s_{o}$
- **unten beschränkt**
  collapsed:: true
	- $B\subseteq\mathbb{R}$ heißt nach unten beschränkt, wenn es eine untere Schranke $s_{u}\in\mathbb{R}$ existiert
	- es gilt $\forall b\in B:b\geq s_{u}$
		- genau: $\exists s_{u}\in\mathbb{R}:\forall b\in B:b\geq s_{u}$
- **beschränkt**
  collapsed:: true
	- $B\subseteq\mathbb{R}$ heißt beschränkt, wenn es eine obere und eine untere Schranke existiert
		- genau: $\exists s_{o},s_{u}\in\mathbb{R}:\forall b\in B:s_{u}\leq b\leq s_{o}$
- **unbeschränkt**
  collapsed:: true
	- eine unbeschränkte Menge kann nach oben oder nach unten beschränkt sein, aber nicht beides
	- effektiv: eine Richtung unbeschränkt
- ! $s_{o},s_{u}$ müssen kein Teil von B sein
-
- **Maxima**
  collapsed:: true
	- für eine Menge $A\subseteq\mathbb{R}$ und ein Element $x\in A$ ist x das Maximum, wenn $\forall a\in A:x\geq a$
	- $x=\max A$
- **Minima**
  collapsed:: true
	- für eine Menge $A\subseteq\mathbb{R}$ und ein Element $x\in A$ ist x das Minimum, wenn $\forall a\in A:x\leq a$
	- $x=\min A$
-
- **Supremum**
  collapsed:: true
	- sei $B\subseteq\mathbb{R}$
	- wenn es eine *kleinste obere Schranke* $s_{o}\in\mathbb{R}$ existiert, dann ist $\sup B:=s_{o}$
	- dabei gilt
		- $s_{o}$ ist eine obere Schranke von B
		  logseq.order-list-type:: number
		- für jede andere obere Schranke $\tilde{s_{o}}$ gilt $\tilde{s_{o}}\geq s_{o}$
		  logseq.order-list-type:: number
- **Infimum**
  collapsed:: true
	- genau wie Supremum, aber mit der *größten oberen Schranke*
	- $\inf B:=s_{u}$
-