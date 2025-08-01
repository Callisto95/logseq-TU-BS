reference:: 13c

-
- Beispiel
	- $\sum_{k=1}^{\infty}\frac{1}{k^{\alpha}}$ konvergiert für welche $\alpha$?
-
- Satz: **Integral- und Wachstumskriterium**
	- reference:: 13.7
	- sei $f:\left\lbrack1,\infty\right)\rightarrow\left\lbrack0,\infty\right)$ monoton fallend
	- Dann gilt: $\sum_{k=1}^{\infty}f\left(k\right)\text{  konvergiert}\Leftrightarrow\int_1^{\infty}f\left(x\right)dx\text{ konvergiert}$
		- sei $a_{k}=f\left(k\right)$
	- Beweis
	  collapsed:: true
		- "<="
			- $\int_1^{\infty}f\left(x\right)dx$ konvergiert
			- für $n\in\mathbb{N},n>1$ gilt
				- $$\sum_{k=2}^{n}f\left(k\right)=\sum_{k=2}^{n}f\left(k\right)\int_{k-1}^{k}1\cdot dx=\sum_{k=2}^{n}\int_{k-1}^{k}\left\lbrack f\left(k\right)\right\rbrack_1dx$$
					- 1: $x\in\left\lbrack k-1,k\right\rbrack:f\left(k\right)\leq f\left(x\right)$
				- $$\leq\sum_{k=2}^{n}\int_{k-1}^{k}f\left(x\right)dx=\int_1^{n}f\left(x\right)dx\leq\int_1^{\infty}f\left(x\right)dx$$
				- $$\Rightarrow\sum_1^{\infty}f\left(k\right)\text{ konvergiert}$$
		- "=>"
			- $$\sum_{k=1}^{\infty}f\left(k\right)\text{ konvergiert}$$
			- $$\text{zZ:}\int_1^{\infty}f\left(x\right)dx=\lim_{\beta\rightarrow\infty}\int_1^{\beta}f\left(x\right)dx\text{ konvergiert}$$
			- Es gibt zu $\varepsilon>0$ ein
				- $$n\in\mathbb{N}:\forall z,y\in\left\lbrack n,\infty\right):\int_{z}^{y}f\left(x\right)dx<\varepsilon$$
			- Wähle $n\in\mathbb{N}$ so, dass $\sum_{k=n}^{\infty}f\left(k\right)<\varepsilon$
			- für $y,z\in\mathbb{R}:y\geq z\geq n$ wähle ein $m\in\mathbb{N}$ mit $m\geq y$
				- $$\Rightarrow\int_{z}^{y}f\left(x\right)dx\leq\int_{n}^{m}f\left(x\right)dx=\sum_{k=n}^{m-1}\int_{k}^{k+1}\left\lbrack f\left(x\right)\right\rbrack_1dx$$
					- 1: monoton fallend, also $f\left(x\right)\leq f\left(k\right)$
				- $$\leq\sum_{k=n}^{m-1}f\left(k\right)\left\lbrack\int_{k}^{k+1}1\cdot dx\right\rbrack_{=1}=\sum_{k=n}^{m-1}f\left(k\right)<\varepsilon$$
-
- Beispiel:
  collapsed:: true
	- reference:: 13.8
	- $$\sum_{k=1}^{n}\frac{1}{k}=\sum_{k=1}^{n}\int_{k}^{k+1}\frac{1}{k}dx\geq\sum_{k=1}^{n}\int_{k}^{k+1}\frac{dx}{x}=\int_1^{n+1}\frac{dx}{x}$$
	- $$=\left\lbrack\ln x\right\rbrack_1^{n+1}=\ln\left(n+1\right)\longrightarrow{}_{n\rightarrow\infty}\infty$$
	- $$\Rightarrow\sum_{k=1}^{\infty}\frac{1}{k}\text{ divergiert}$$
- Beispiel:
	- reference:: 13.9
	- $$\alpha\in\left(1,\infty\right),n\in\mathbb{N}$$
	- $$\sum_{k=2}^{n}\frac{1}{k^{\alpha}}=\sum_{k=2}^{n}\int_{k-1}^{k}\frac{dx}{k^{\alpha}}\leq\sum_{k=2}^{n}\int_{k-2}^{k}\frac{dx}{x^{\alpha}}=\int_1^{n}\frac{dx}{x^{\alpha}}=\int_1^{n}x^{-\alpha}dx$$
	- $$=\left\lbrack\frac{1}{1-\alpha}x^{1-\alpha}\right\rbrack_1^{n}=\frac{1}{1-\alpha}\left(\frac{1}{n^{\alpha-1}}-1\right)\longrightarrow{}_{n\rightarrow\infty}\frac{1}{\alpha-1}$$
-