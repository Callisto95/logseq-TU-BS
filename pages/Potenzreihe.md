alias:: PR

-
- Definition
	- reference:: 6.5
	- $\left(a_{k}\right)\subseteq\mathbb{C},x_0\in\mathbb{C}$
		- $x_0$ *Entwicklungspunkt*
	- $$x\mapsto\left(\sum_{k=0}^{n}a_{k}\left(x-x_0\right)^{k}\right)_{n=0}^{\infty},\mathbb{C}\mapsto\text{Map}\left(\mathbb{N}_0,\mathbb{C}\right)$$
		- Zuordnung von x zu einer Reihe mit Gliedern $a_{k}\left(x-x_0\right)^{k}$, die von x abhängen
	- Wunsch: $f:\mathbb{C}\rightarrowtail\mathbb{C}$ oder $f:\mathbb{R}\rightarrowtail\mathbb{R}$
	- $\text{Dom}\left(f\right)=\left\lbrace x\in\mathbb{C}:\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}\text{ konvergent}\right\rbrace$
	- $f\left(x\right):=\lim_{n\rightarrow\infty}\sum_{k=1}^{n}a_{k}\left(x-x_0\right)^{k}$
-
- Konvergenzradius:
	- $$r\coloneqq\frac{1}{\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left(a_{k}\right)}}\in\left\lbrack0,\infty\right\rbrack$$
		- Als Ausnahme: $\frac10=\infty,\frac{1}{\infty}=0$
-
- Satz: [[cauchy]] -Hadamard
	- reference:: 6.6
	- Für eine PR $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}\subseteq\mathbb{C}$ mit KR $r\in\left\lbrack0,\infty\right\rbrack$ gilt
		- für $x\in\mathbb{C}$ mit $\left|x-x_0\right|<r$ konvergiert $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}$ absolut
		  logseq.order-list-type:: number
		- für $x\in\mathbb{C}$ mit $\left|x-x_0\right|>r$ divergiert die Reihe $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}$
		  logseq.order-list-type:: number
			- Beweis: Wende das [[Wurzelkriterium]] auf die Reihe $\sum_{k=0}^{\infty}b_{k}\left(x\right)$ mit $b_{k}\left(x\right)=a_{k}\cdot\left(x-x_0\right)^{k}$ an
				- $$\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|b_{k}\left(x\right)\right|}=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|\cdot\left|x-x_0\right|^{k}}=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\left(\sqrt[k]{\left|a_{k}\right|}\cdot\sqrt[k]{\left|x-x_0\right|^{k}}\right)$$
				- $$=\left|x-x_0\right|\cdot\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}=\left|x-x_0\right|\cdot\frac{1}{r}$$
				- für [[absolute-Konvergenz]]: $\left|x-x_0\right|\cdot\frac{1}{r}<1\Leftrightarrow\left|x-x_0\right|<r$
				- für Divergenz: $\left|x-x_0\right|\cdot\frac{1}{r}>1\Leftrightarrow\left|x-x_0\right|>r$
			- $r=\frac{1}{\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}}$ **Konvergenzradius**
-
- Lemma
	- reference:: 6.7
	- $\left(a_{k}\right)\subseteq\mathbb{C}\backslash\left\lbrace0\right\rbrace$ für die $\tilde{r}\coloneqq\lim_{k\rightarrow\infty}\frac{\left|a_{k}\right|}{\left|a_{k+1}\right|}$ existiert
	- => $\tilde{r}=r$
	- Beweis
		- Idee: $\tilde{r}$ tut, was r tut
		- Wende [[Quotientenkriterium]] auf $\sum_{k=0}^{\infty}b_{k}\left(x\right),b_{k}\left(x\right)=a_{k}\left(x-x_0\right)^{k}$
		- $$\lim_{k\rightarrow\infty}\frac{\left|b_{k+1}\left(x\right)\right|}{\left|b_{k}\left(x\right)\right|}=\lim_{k\rightarrow\infty}\frac{\left|a_{k+1}\right|\cdot\left|x-x_0\right|^{k+1}}{\left|a_{k}\right|\cdot\left|x-x_0\right|^{k}}=\left|x-x_0\right|\cdot\lim_{k\rightarrow\infty}\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}=\frac{\left|x-x_0\right|}{\tilde{r}}$$
-