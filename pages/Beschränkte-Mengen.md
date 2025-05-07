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
	- sei $B\subseteq\mathbb{R}$
	- wenn es eine *kleinste obere Schranke* $s_{o}\in\mathbb{R}$ existiert, dann ist $\sup B:=s_{o}$
	- dabei gilt
		- $s_{o}$ ist eine obere Schranke von B
		  logseq.order-list-type:: number
		- für jede andere obere Schranke $\tilde{s_{o}}$ gilt $\tilde{s_{o}}\geq s_{o}$
		  logseq.order-list-type:: number
	- **Supremumsprinzip**: Jede nicht leere, nach oben beschränkte Menge $M\subseteq\mathbb{R}$ hat ein Supremum
- **Infimum**
	- genau wie Supremum, aber mit der *größten unteren Schranke*
	- $\inf B:=s_{u}$
-
- $-\sup\left(M\right)=\inf\left(-M\right)$
  collapsed:: true
	- reference:: 1.16
	- dabei $-M:-\left\lbrace-x;x\in M\right\rbrace$
	- a: $\forall y\in-M:y\geq-\sup\left(M\right)$
		- sei $y\in-M$
		- => $\exists x\in M:y=-x$
		- => $x\leq\sup\left(M\right)$ /$\cdot-1$
		- => $\frac{-x}{-y}\geq-\sup\left(M\right)$
	- b: $-\sup\left(M\right)$ ist die kleinste untere Schranke
		- sei $s\in\mathbb{R}$ eine untere Schranke von -M
		- also $\forall x\in M:-x\geq s$ /$\cdot-1$
		- => $\forall x\in M:x\leq-s$
		- => s ist eine obere Schranke von M
		- => $\sup\left(M\right)\leq-s$ /$\cdot-1$
		- => $-\sup\left(M\right)\geq s$
		- => $-\sup\left(M\right)$ ist die größte untere Schranke von -M
-
- **Archimedes**
	- Die natürlichen Zahlen $\mathbb{N}\subseteq\mathbb{R}$ sind nach oben unbeschränkt.
	- also: $\forall r\in\mathbb{R}:\exists n\in\mathbb{N}:n>c$
	- Beweis
	  collapsed:: true
		- sei $s\in\mathbb{R}$ eine obere Schranke von $\mathbb{N}$
		- damit wäre auch $s-1<s$ eine obere Schranke von $\mathbb{N}$
		- Für ein $s\in\mathbb{R}$ gilte: $\forall n\in\mathbb{N}:n\leq s$
		- $n+1\leq s$ muss auch gelten
		- also $\forall n\in\mathbb{N}:n\leq s-1$