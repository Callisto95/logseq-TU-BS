# Potenz
	- reference:: 10.21
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack,p\in\left\lbrack1,\infty\right)$ ist $\left|f\right|^{p}\in\mathbb{R}\left\lbrack a,b\right\rbrack$
	- Ziel
	  collapsed:: true
		- $$f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
		- Hilfsmittel:
			- $$f\left(x\right)\cdot g\left(x\right)=\frac14\left(\left(f\left(x\right)+g\left(x\right)\right)^2-\left(f\left(x\right)-g\left(x\right)\right)^2\right)$$
		- Brauche:
			- $$f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Rightarrow f^2\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- Beweis
	  collapsed:: true
		- o.B.d.A. $\forall x\in\left\lbrack a,b\right\rbrack:0\leq f\left(x\right)\leq1$
			- f: einsetze f durch $\left|f\right|$
			- $\leq1$: teile durch $M\coloneqq\sup_{x\in\left\lbrack a,b\right\rbrack}\left|f\left(x\right)\right|>0$
			- zu $\varepsilon>0$ gibt es $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $0\leq\varphi\leq f\leq\psi\leq1$ und $\int_{a}^{b}\left(\psi-\varphi\right)<\frac{\varepsilon}{p}$
			- Erhalte $0\leq\varphi^{p}\leq f^{p}\leq\psi^{p}\leq1$
			- MWS der Differenzialrechnung: $h\left(t\right)\coloneqq t^{p}$
				- $0\leq h^{\prime}\left(t\right)=p\cdot t^{p-1}\leq p$
			- für $s,t\in\left\lbrack0,1\right\rbrack$ gibt es ein $\xi\in\left\lbrack0,1\right)$ mit
				- $$\frac{s^{p}-t^{p}}{s-t}=h^{\prime}\left(\xi\right)\leq p$$
				- $$\Rightarrow s^{p}-t^{p}\leq p\cdot\left(s-t\right)$$
				- $$\Rightarrow\int_{a}^{b}\left(\psi^{p}-\varphi^{p}\right)\leq p\cdot\int_{a}^{b}\left(\psi-\varphi\right)<p\cdot\frac{\varepsilon}{p}=\varepsilon$$
-
- # Produkt
	- sei $f,g\in\mathbb{R}\left\lbrack a,b\right\rbrack$
	- Dann ist auch $f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$
	- dabei
	  $$\int_{a}^{b}f\left(x\right)\cdot d\left(x\right)dx\neq\int_{a}^{b}f\left(x\right)dx\cdot\int_{a}^{b}g\left(x\right)dx$$
-