- **Intro**
  collapsed:: true
	- **Relationen**
	  collapsed:: true
		- reference:: 0.14
		- seien A und Z Mengen
		- $R\subseteq A\times Z$ heißt eine Relation
		- R ist *funktional* wenn $\forall\left(a,z\right),\left(a^{\prime},z^{\prime}\right)\in\mathbb{R}:a=a^{\prime}\Rightarrow z=z^{\prime}$ gilt
			- $\left(a,z\right)\in R$: a ist das Urbild wird auf das Bild z abgebildet
	- **partielle Funktionen**
		- reference:: 0.15
		- $f=\left(A,Z,R\right)$
		- Ausgangsmenge A
		- Zielmenge
		- funktionale Relation R mit $R\subseteq A\times Z$, wobei $f:A\supset\mapsto Z$
		- R ist der *Graph* von f
		  collapsed:: true
			- $Gra\space f=R$
		- *Definitionsbereich* von f: $Dom\space f\coloneqq \left\lbrace x\in A;\exists y\in\mathbb{Z}:\left(x,y\right)\in Gra\space f\right\rbrace$
		  collapsed:: true
			- jedes $x\in Dom\space f$ hat ein eindeutig bestimmtes y mit $\left(x,y\right)\in Gra\space f$
		- die Abbildung von x auf f wird geschrieben als $x\mapsto f\left(x\right)$
		- *Bild von f*: $Ran\space f\coloneqq \left\lbrace y\in Z;\exists x\in Dom\space f:y\in f\left(x\right)\right\rbrace$
			- *Bild von M unter f*: alle Werte von M werden mit f zu einer neuen Menge abgebildet werden
			- *Urbild von N unter f* ($f^{-1}$): alle Werte von N werden auf einem Wert abgebildet, bei denen f den Wert in N erzeugt
		- *Menge alle Abbildungen von A nach Z*: $Map\left(A,Z\right)\coloneqq Z^{A}\coloneqq \left\lbrace f;f:A\rightarrow Z\right\rbrace$
	- [[Eigenschaften-von-Abbildungen]]
	- **Binomialkoeffizient**
	  collapsed:: true
		- $\begin{pmatrix}n\\ k\end{pmatrix}\coloneqq \frac{n!}{k!\left(n-k\right)!}$, wenn $0\leq k\leq n$, ansonsten 0
			- "n über k"
	- **Pascalsches Dreieck**
	  collapsed:: true
		- $\begin{pmatrix}n\\ k-1\end{pmatrix}+\begin{pmatrix}n\\ k\end{pmatrix}=\begin{pmatrix}n+1\\ k\end{pmatrix}$
	- **binomische Formel**
	  collapsed:: true
		- $\left(a+b\right)^{n}=\sum_{k=0}^{n}\begin{pmatrix}n\\ k\end{pmatrix}a^{k}b^{n-k}$
		- $\left(1+a\right)^{n}=\sum_{k=0}^{n}\begin{pmatrix}n\\ k\end{pmatrix}x^{k}$
-
- **Rechenregeln von Zeugs**
	- $\ln$
		- $\ln a^{b}=\ln\left(a\right)\cdot b$
		- $\ln\left(a\cdot b\right)=\ln a+\ln b$
	- $\exp$
		- $\exp\left(a+b\right)=\exp a\cdot\exp b$
		  id:: 68399f50-9828-4f4a-9dd6-f208050041b4
		- $\exp\left(a\cdot b\right)=\exp\left(a\right)^{b}$
	- Divergenz
		- $\sum_{k=1}^{\infty}\frac{1}{k^{\alpha}}$ divergiert bei $\alpha\leq1$, konvergiert bei $\alpha>1$
			- (genauer: $\text{Re }\alpha\leq1$)
	- Konvergenz
		- $\sum_{k=1}^{\infty}a_{k}\text{ konvergiert}\not\Rightarrow\sum_{k=1}^{\infty}a_{k}^2\text{ konvergiert}$
		- $\sum_{k=1}^{\infty}a_{k}\text{ konvergiert absolut}\Rightarrow\sum_{k=1}^{\infty}a_{k}^2\text{ konvergiert absolut}$
-
- [[Reelle-Zahlen]]
- [[Ungleichungen]]
-
- **streng monoton fallende Funktion**
  collapsed:: true
	- $\forall a,b\in Dom\space f:a<b\Rightarrow f\left(a\right)<f\left(b\right)$
-
- [[Folgen]]
- [[Konvergenz]]
-
- [[arithmetisches-und-geometrisches-Mittel]]
-
- [[Vollständigkeit]]
-
- [[Reihe]]
-
- [[stetige-Funktionen]]
- [[Grenzwertsätze-für-Funktionen-und-stetige-Fortsetzungen]]
-
- [[komplexe-Folgen-und-Reihen]]
-
- [[differenzierbare-Funktionen]]
-
- [[Riemann-Darboux-Integral]]
-