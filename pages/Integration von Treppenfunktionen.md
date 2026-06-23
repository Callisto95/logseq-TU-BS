reference:: 10a

-
- # Zerlegung von Intervallen
	- reference:: 10.1
	- für $\left\lbrack a,b\right\rbrack\subseteq\mathbb{R}$ heißt ein Tupel $\left(x_{k}\right)_{k=0}^{n}=\left(x_{0,}...,x_{n}\right)\in\mathbb{R}^{n+1}$ eine **Zerlegung** von $\left\lbrack a,b\right\rbrack$, wenn $a=x_0<x_1<...<x_{n}=b$
		- dabei $\mathbb{Z}\left\lbrack a,b\right\rbrack$: Menge aller Zerlegungen von $\left\lbrack a,b\right\rbrack$
	- für $\left(x_{k}\right)\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ heißt $\Phi\left(\left(x\right)_{k=1}^{n}\right)\coloneqq\max_{1\leq k\leq n}\left(x_{k}-x_{k-1}\right)=\max\left\lbrace\Delta x_1,...,\Delta x_{n}\right\rbrace$ die **Feinheit** der Zerlegung
- ## Verfeinerung
	- $\left(x_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ heißt eine Verfeinerung von $\left(y_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack a,b\right\rbrack$, wenn $\left\lbrace x_1,...,x_{n}\right\rbrace\subseteq\left\lbrace y_1,...,y_{n}\right\rbrace$
		- schreibe: $\left(x_{k}\right)_{k=0}^{n}\subseteq\left(y_{k}\right)_{k=0}^{m}$
- ### kleinste gemeinsame Verfeinerung
	- reference:: 10.2
	- für $\left(x_{k}\right)_{k=0}^{\infty},\left(y_{k}\right)_{k=0}^{\infty}$ sei $\left(x_{k}\right)_{k=0}^{\infty}\cup\left(y_{k}\right)_{k=0}^{\infty}$ die Zerlegung mit den Zerlegungspunkten $\left\lbrace x_0,...,x_{n}\right\rbrace\cup\left\lbrace y_0,...,y_{m}\right\rbrace$ die kleinste gemeinsame Verfeinerung von $\left(x_{k}\right)_{k=0}^{\infty}$ und $\left(y_{k}\right)_{k=0}^{\infty}$
-
- # Treppenfunktion
	- reference:: 10.3
	- für $\left\lbrack a,b\right\rbrack\subseteq\mathbb{R}$ heißt $\varphi:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ eine Treppenfunktion, wenn es eine Zerlegung $\left(x_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ und Zahlen $c_0,...,c_{n}\in\mathbb{R}$ gibt mit
	  $$\forall k\in\left\lbrace1,...,n\right\rbrace:\forall x\in\left(x_{k-1},x_{k}\right):\varphi\left(x\right)=c_{k}$$
		- $\text{Trep}\left\lbrack a,b\right\rbrack$: Menge der Treppenfunktionen auf [a,b]
- ## Rechenregeln von Treppenfunktionen
	- reference:: 10.4
	- $\text{Trep}\left\lbrack a,b\right\rbrack$ ist ein [[Vektorraum]]
		- $0\in\text{Trep}\left\lbrack a,b\right\rbrack$
		- für $\varphi,\psi\in\text{Trep}\left\lbrack a,b\right\rbrack,c\in\mathbb{R}$ gilt
			- $c\cdot\varphi\in\text{Trep}\left\lbrack a,b\right\rbrack$
			- $\varphi+\psi\in\text{Trep}\left\lbrack a,b\right\rbrack$
	- Beweis
	  collapsed:: true
		- seien $\left(y_{k}\right),\left(z_{k}\right)\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ mit $\varphi\left(x\right)=a_{k}$ für $y_{k-1}<x<y_{k}$; $\psi\left(x\right)=b_{k}$ für $z_{k-1}<x<z_{k}$
		- => für die kleinste gemeinsame Verfeinerung $\left(y_{k}\right)\cup\left(z_{k}\right)$ sind $\varphi$ und $\psi$ zeischen benachbarten Zerlegungsstellen konstant
- ## Integral von Treppenfunktionen
	- reference:: 10.5
	- $\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\left(x_{k}\right)\in\mathbb{Z}\left\lbrack a,b\right\rbrack,\varphi\left(x\right)=c_{k}$ für alle $x_{k-1}<x<x_{k}$
	  $$\int_{a}^{b}\varphi\coloneqq\int_{a}^{b}\varphi\left(x\right)dx\coloneqq\sum_{k=1}^{n}c_{k}\cdot\left(x_{k}-x_{k-1}\right)=\sum_{k=1}^{n}c_{k}\cdot\left(\Delta x_{k}\right)$$
	  heißt das *bestimmte Integral* von $\varphi$ über [a,b]
- ## linearität des Integrierens
	- reference:: 10.6
	- für $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,s,t\in\mathbb{R}$ gilt
	  $$\int_{a}^{b}\left(s\varphi+t\psi\right)=s\cdot\int_{a}^{b}\varphi+t\cdot\int_{a}^{b}\varphi$$
	- Beweis
	  collapsed:: true
		- sei $\left(x_{k}\right)\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ mit $\varphi\left(x\right)=a_{k}\land\varphi\left(x\right)=b_{k}$ für alle $x_{k-1}<x<x_{k}$
		- bla bla bla, ja das passt
-
- # Monotonie des Integrals
	- reference:: 10.7
	- für $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq\psi$ (d.h. $\forall x\in\left\lbrack a,b\right\rbrack:\varphi\left(x\right)\leq\psi\left(x\right)$) gilt
	- $$\int_{a}^{b}\varphi\leq\int_{a}^{b}\psi$$
	- Beweis
		- sei $\left(x_{k}\right)\in\mathbb{Z}\left\lbrack a,b\right\rbrack$ so, dass $\varphi\left(x\right)=a_{k}\land\psi\left(x\right)=b_{k}$ für alle $x_{k-1}<x<x_{k}$
		- dabei: $a_{k}\leq b_{k}$
		- => $\int_{a}^{b}\varphi=\sum_{k=1}^{n}a_{k}\cdot\Delta x_{k}\leq\sum_{k=1}^{n}b_{k}\Delta x_{k}=\int_{a}^{b}\varphi$
-
- [[Darboux Summen und bestimme Integrale]]
-