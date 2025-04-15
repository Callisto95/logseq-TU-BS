- bekannt: $a:\left\lbrace1,...,n\right\rbrace\rightarrow M$
- neu: $a:\mathbb{N}\rightarrow M$
- "unendliche Liste" $\left(a_1,...,a_{n}\right)$
-
- unter einer Folge verstehen wir eine Abbildung $a:\mathbb{N}\rightarrow M$, wobei M eine beliebige Menge ist
  collapsed:: true
	- $a_{k}:=a\left(k\right)\in M$ heißen Gleider der Folge
	- Notation: $\left(a_{k}\right):=\left(a_{k}\right)_{k\in\mathbb{N}}:=\left(a_{k}\right)_{k\in a}^{\infty}:=a$
		- ! $a_{k}\neq\left(a_{k}\right)$
	- Die Menge aller Folgen in M ist $M^{\mathbb{N}}=Map\left(\mathbb{N},M\right)$
	- Es kann auch einfach $\left(a_{k}\right)\subseteq M$ anstatt $\left(a_{k}\right)_{k=1}^{\infty}\in M^{\mathbb{N}}$ geschrieben werden
	- Beispiele für Folgen
		- $\left(a_{k}\right)_{k=1}^{\infty}$ mit $a_{k}=k$ also $\left(a_{k}\right)=\left(1,2,3,...\right)$
		  logseq.order-list-type:: number
		- $\left(b_{k}\right)\in\mathbb{R}^{\mathbb{N}},b_{k}:=\frac{1}{k}$ also $\left(b_{k}\right)=\left(1,\frac12,\frac13,...\right)$
		  logseq.order-list-type:: number
		- $\left(c_{k}\right)\in\mathbb{R}_{}^{\mathbb{N}_0},c_{k}=2^{k}$ also $\left(c_{k}\right)=\left(1,2,4,8,16,32,...\right)$
		  logseq.order-list-type:: number
-
- **rekursiv definierte Folgen**
	- Beispiel: Bevölkerungsmodell
		- Größe $\left(b_{k}\right)$ einer Bevölkerung wird zu einem Zeitpunkt $k\in\mathbb{N}$ beschrieben
		- Startwert $a>0$
		- Wachstumsfaktor: $w>0$
		- Limitierung: $L>0$
		- mit $b_1=a$, dann $\forall k\in\mathbb{N}:b_{k+1}:=b_{k}+w\left(L-b_{k}\right)b_{k}$
		-