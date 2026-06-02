reference:: 6.6

- Satz
- Für eine [[Potenzreihe]] $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}\subseteq\mathbb{C}$ mit Konvergenzradius $r\in\left\lbrack0,\infty\right\rbrack$ gilt
	- für $x\in\mathbb{C}$ mit $\left|x-x_0\right|<r$ konvergiert $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}$ absolut
	  logseq.order-list-type:: number
	- für $x\in\mathbb{C}$ mit $\left|x-x_0\right|>r$ divergiert die Reihe $\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}$
	  logseq.order-list-type:: number
		- Beweis: Wende das [[Wurzelkriterium]] auf die Reihe $\sum_{k=0}^{\infty}b_{k}\left(x\right)$ mit $b_{k}\left(x\right)=a_{k}\cdot\left(x-x_0\right)^{k}$ an
			- $$\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|b_{k}\left(x\right)\right|}=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|\cdot\left|x-x_0\right|^{k}}=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\left(\sqrt[k]{\left|a_{k}\right|}\cdot\sqrt[k]{\left|x-x_0\right|^{k}}\right)$$
			- $$=\left|x-x_0\right|\cdot\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}=\left|x-x_0\right|\cdot\frac{1}{r}$$
			- für [[absolute Konvergenz]]: $\left|x-x_0\right|\cdot\frac{1}{r}<1\Leftrightarrow\left|x-x_0\right|<r$
			- für Divergenz: $\left|x-x_0\right|\cdot\frac{1}{r}>1\Leftrightarrow\left|x-x_0\right|>r$
		- $r=\frac{1}{\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}}$ **Konvergenzradius**
-