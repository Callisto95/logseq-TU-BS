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
- # Summe
	- $$\int_{a}^{b}\left(f\left(x\right)+g\left(x\right)\right)dx=\int_{a}^{b}f\left(x\right)dx+\int_{a}^{b}g\left(x\right)dx$$
-
- # Skalarmultiplikation
	- $f,g\in\mathbb{R}\left\lbrack a,b\right\rbrack,\lambda\in\mathbb{R}$
	- es gilt
	  $$\lambda f\in\mathbb{R}\left\lbrack a,b\right\rbrack,f+g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	  und
	  $$\int_{a}^{b}\lambda f\left(x\right)dx=\lambda\cdot\int_{a}^{b}f\left(x\right)dx$$
	- Beweise
	  collapsed:: true
		- Homogenität
			- o.B.d.A. $\lambda\neq0$
			- Fall $\lambda>0$
				- wähle $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und $\int_{a}^{b}\left(\psi-\varphi\right)<\frac{\varepsilon}{\lambda}$
				- => $\lambda\cdot\varphi,\lambda\cdot\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,\lambda\cdot\varphi\leq\lambda\cdot f\leq\lambda\cdot\psi$
				- $$\int_{a}^{b}\left(\lambda\cdot\psi-\lambda\cdot\varphi\right)=\lambda\cdot\int_{a}^{b}\left(\psi-\varphi\right)<\lambda\cdot\frac{\varepsilon}{\lambda}=\varepsilon$$
				- $$\Rightarrow\lambda f\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
				- noch zZ: $\int_{a}^{b}\lambda f=\lambda\cdot\int_{a}^{b}f$
				- $$\lambda\cdot\int_{a}^{b}f-\varepsilon\leq\lambda\cdot\int_{a}^{b}\varphi=\int_{a}^{b}\lambda\cdot\varphi\leq\int_{a}^{b}\lambda\cdot f\leq\int_{a}^{b}\lambda\cdot\psi=\lambda\int_{a}^{b}\psi\leq\lambda\int_{a}^{b}f+\varepsilon$$
				- $$\Rightarrow\forall\varepsilon>0:\lambda\int_{a}^{b}f-\varepsilon\leq\int_{a}^{b}\lambda f\leq\lambda\int_{a}^{b}f+\varepsilon$$
				- $$\Rightarrow^{\varepsilon\downarrow0}\lambda\int_{a}^{b}f\leq\int_{a}^{b}\lambda f\leq\lambda\int_{a}^{b}f$$
			- Fall $\lambda=-1$
				- $$\varphi\leq f\leq\psi,\int_{a}^{b}\left(\psi,\varphi\right)<\varepsilon$$
				- $$\Rightarrow-\psi\leq-f\leq-\varphi$$
				- $$\int_{a}^{b}\left(-\varphi-\left(-\psi\right)\right)=\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$$
				- für $\lambda>0:\lambda=-1\cdot\lambda$
		- Additivität
			- zu $\varepsilon>0:\varphi,\psi,\eta,\vartheta\in\text{Trp}\left\lbrack a,b\right\rbrack:\varphi\leq f\leq\psi,\eta\leq g\leq\vartheta$ und
			- $$\int_{a}^{b}\left(\psi-\varphi\right)<\frac{\varepsilon}{2},\int_{a}^{b}\left(\vartheta-\eta\right)<\frac{\varepsilon}{2}$$
			- $$\Rightarrow\varphi+\eta\in\text{Trp}\left\lbrack a,b\right\rbrack,\psi+\vartheta\in\text{Trp}\left\lbrack a,b\right\rbrack$$
			- $$\varphi+\eta\leq f+g\leq\psi+\vartheta$$
			- $$\int_{a}^{b}\left(\left(\psi+\vartheta\right)-\left(\varphi+\eta\right)\right)=\int_{a}^{b}\left(\left(\psi-\varphi\right)+\left(\vartheta-\eta\right)\right)=\int_{a}^{b}\left(\psi-\varphi\right)+\int_{a}^{b}\left(\vartheta-\eta\right)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
			- also $\int_{a}^{b}\left(f+g\right)=\int_{a}^{b}f+\int_{a}^{b}g$ wie oben
-
- # Vertauschen von Grenzen
	- sei $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$
	- $$\forall c\in\left\lbrack a,b\right\rbrack:$$