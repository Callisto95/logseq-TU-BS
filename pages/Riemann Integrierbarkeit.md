reference:: 10.9

- Eine beschränkte Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ heißt (Riemann) integrierbar, wenn
  $$\int_{a}^{b}f\coloneqq_{\ast}\int_{a}^{b}f=^{\ast}\int_{a}^{b}f$$
  gilt
- $\mathbb{R}\left\lbrack a,b\right\rbrack$: Menge der integrierbaren Funktionen auf $\left\lbrack a,b\right\rbrack$
	- Notiz: das R ist eigentlich nicht das reele Zahlen-$\mathbb{R}$, sondern ein $\mathcal{R}$
-
- # Einschließung durch Treppenfunktionen
	- reference:: 10.10
	- Eine Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ ist genau dann integrierbar, wenn es zu jedem $\varepsilon>0$ Treppenfunktionen $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ gibt mit $\varphi\leq f\leq\psi$. Also
	  $$\forall x\in\left\lbrack a,b\right\rbrack:\varphi\left(x\right)\leq f\left(x\right)\leq\psi\left(x\right)$$
	- $$\int_{a}^{b}\left(\psi\left(x\right)-\varphi\left(x\right)\right)dx<\varepsilon$$
	  $$=\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx<\varepsilon$$
	- Beweis
	  collapsed:: true
		- "=>"
			- seien $f\in\mathbb{R}\left\lbrack a,b\right\rbrack,\varepsilon>0$
			- $$^{\ast}\int_{a}^{b}f=_{\ast}\int_{a}^{b}f$$
			- es gibt ein $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und
			- $$\int_{a}^{b}\varphi\left(x\right)dx>_{\ast}\int_{a}^{b}f\left(x\right)dx-\frac{\varepsilon}{2}$$
				- -> keine obere Schranke
			- $$\int_{a}^{b}\psi\left(x\right)<^{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}$$
				- -> keine untere Schranke
			- $\int_{a}^{b}$ ist linear für Treppenfunktionen
			- $$\Rightarrow\int_{a}^{b}\left(\varphi\left(x\right)-\varphi\left(x\right)\right)dx=\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx$$
			- $$<^{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}-_{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}$$
			- $$\Rightarrow\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
		- "<="
			- für $\varepsilon>0$ gibt es $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und
			- $$^{\ast}\int_{a}^{b}f\left(x\right)dx-_{\ast}\int_{a}^{b}f\left(x\right)dx\leq\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx<\varepsilon$$
			- Im Limes $\varepsilon\downarrow0$ folgt $_{\ast}\int_{a}^{b}f\left(x\right)dx=^{\ast}\int_{a}^{b}f\left(x\right)dx$
-
- # Bereichsadditivität
	- reference:: 10.11
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},c\in\left(a,b\right)$
	- Dann $f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Leftrightarrow f\in\left\lbrack a,c\right\rbrack\text{ und }f\in\mathbb{R}\left\lbrack c,b\right\rbrack$
	- Dann gilt:
	  $$\int_{a}^{b}f\left(x\right)dx=\int_{a}^{c}f\left(x\right)dx+\int_{c}^{b}f\left(x\right)dx$$
	- Übung:
	  collapsed:: true
		- reference:: 10.12
		- $f:\left\lbrack1,2\right\rbrack\rightarrow\mathbb{R},f\left(x\right)\coloneqq\frac{1}{x}$
		- zZ: $f\in\mathbb{R}\left\lbrack1,2\right\rbrack$
		- für $n\in\mathbb{N}:\Delta x\coloneqq\frac{1}{n}$
		- $x_{k}\coloneqq1+k\cdot\Delta x=1+\frac{k}{n}$
		- => $\left(x_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack1,2\right\rbrack$
		- Für die untere Treppenfunktion:
			- $$a_{k}\coloneqq\frac{1}{x_{k}}=\frac{1}{1+\frac{k}{n}}=\frac{1}{\frac{n+k}{n}}=\frac{n}{n+k}$$
		- Für die obere Treppenfunktion:
			- $$b_{k}\coloneqq\frac{1}{x_{k-1}}=\frac{n}{n+k-1}$$
		- Untersumme:
			- $$\int_{a}^{b}\varphi_{n}=\sum_{k=1}^{n}\frac{n}{n+k}\cdot\frac{1}{n}=\sum_{k=1}^{n}\frac{1}{n+k}=\frac{1}{n+1}+...+\frac{1}{2n}$$
		- Obersumme:
			- $$\int_{a}^{b}\psi_{n}=\sum_{k=1}^{b}\frac{n}{n+k-1}\cdot\frac{1}{n}=\sum_{k=1}^{n}\frac{1}{n+k-1}=\frac{1}{n}+...+\frac{1}{2n-1}$$
		- $$\Rightarrow\int_{a}^{b}\left(\psi_{n}-\varphi_{n}\right)=\frac{1}{n}-\frac{1}{2n}=\frac{1}{2n}\longrightarrow{}_{n\rightarrow\infty}0$$
		- Notiz
			- $$\int_1^2\frac{1}{x}dx=\lim_{n\rightarrow\infty}\sum_{k=1}^{n}\frac{1}{n+k}=\lim_{k\rightarrow\infty}\left(\frac{1}{k+1}+...+\frac{1}{2n}\right)$$
-