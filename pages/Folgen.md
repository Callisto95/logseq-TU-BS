- [[Monotone-Folgen]]
- [[Grenzwertsätze-für-Folgen]]
- [[Cauchy-Folgen]]
-
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
  collapsed:: true
	- Beispiel: Bevölkerungsmodell
		- Größe $\left(b_{k}\right)$ einer Bevölkerung wird zu einem Zeitpunkt $k\in\mathbb{N}$ beschrieben
		- Startwert $a>0$
		- Wachstumsfaktor: $w>0$
		- Limitierung: $L>0$
		- mit $b_1=a$, dann $\forall k\in\mathbb{N}:b_{k+1}:=b_{k}+w\left(L-b_{k}\right)b_{k}$
-
- **geometrische Summen**
	- Sei $q\in\mathbb{R}$. Definiere $\left(a_{n}\right)_{n=0}^{\infty}\subseteq\mathbb{R}$ durch $a_0=1,a_{n}:=a_{n-1}+q^{n}$
	- Es gilt $\forall q\in\mathbb{R}\setminus\left\lbrace1\right\rbrace:\forall n\in\mathbb{N}_0:a_{n}=\sum_{k=0}^{n}q^{k}=\frac{1-q^{n-1}}{1-q}$
	- Beispiel: Würfelsumme
	  collapsed:: true
		- addieren des Volumens von Würfeln mit k Seitenlänge
		- $\forall n\in\mathbb{N}:\sum_{k=1}^{n}k^3=\frac14n^2\left(n+1\right)^2$
	- Beispiel: Fibonacci-Zahlen
	  collapsed:: true
		- |Generation|0|1|2|3|4|5|...|
		  |--|--|--|--|--|--|--|--|
		  |Kaninchen|1|1|2|3|5|8|...|
		  |--|--|--|--|--|--|--|--|
		  |Zuwachs|0|0|1|1|2|3|...|
		- $a_0:=1,a_1:=1$
		- $a_{n+2}:=a_{n}+a_{n+1}$
		- Es gilt: $\forall n\in\mathbb{N}_0:a_{n}\leq\left(\frac{1+\sqrt5}{2}\right)^{n}=:A\left(n\right)$
		- $\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_{n}}=\frac{1+\sqrt5}{2}$ goldener Schnitt
	- Beispiel: Kreisumfang
	  collapsed:: true
		- Kreis mit Radius r=1
		- Approximation:
			- regelmäßiges Sechseck mit Seitenlänge $S_1=1$
			- Umfang: $U_1=6\cdot1\leq2\pi$
			- Näherungswert: $\pi_1=3\approx\pi$
		- Schreibe ein $3\cdot2^{k}$-Eck ein
		- Umfang: $U_{k}=3\cdot2^{k}\cdot S_{k}\approx2\pi$
		- Seitenlänge: // Bild
		- Pythagoras:
			- $\left(\frac{S_{k}}{2}\right)^2+x^2=S_{k+1}^2$
			- $\left(1-x\right)^2=1-\left(\frac{S_{k}}{2}\right)^2$
			- $\Rightarrow1-x=\sqrt{1-\left(\frac{S_{k}}{2}\right)^2}$
			- $\Rightarrow x=1-\sqrt{1-\left(\frac{S_{k}}{2}\right)^2}$
			- Also $S_{k+1}=\sqrt{\left(\frac{S_{k}}{2}\right)^2+x^2}=...=\sqrt{2-2\sqrt{1-\left(\frac{S_{k}}{2}\right)^2}}$
			- Erwarte: $\lim_{k\rightarrow\infty}U_{k}=2\pi$
		- $\left(\pi_{k}\right)_{k=1}^{\infty}=\left(3,3.1,3.14,3.141,...\right)$
		-
	- Beispiel: Dekadische Entwicklung
	  collapsed:: true
		- $x\in\left\lbrack0,10\right),\left(z_{n}\right)_{n=0}^{\infty}\subseteq\left\lbrace0,...,9\right\rbrace$
		- Näherungswert: $x_{n}=\sum_{k=0}^{n}z_{n}\cdot\frac{1}{10^{k}}$
		- $\Rightarrow\forall n\in\mathbb{N}_0:\left|x-x_{n}\right|\leq\frac{1}{10^{n}}$
		- $x:=\lfloor x\rfloor=\max\left\lbrace\xi\in\mathbb{Z}:\xi\leq x\right\rbrace$
		- $z_{n+1}:=\lfloor10^{n+1}\left(x-x_{n}\right)\rfloor$
		-
-