reference:: 4.18

- Sei $\left(a_{k}\right)\subseteq\mathbb{R}$
- Wenn $w\coloneqq \operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}<1$, dann konvergiert $\sum_{k=1}^{\infty}a_{k}$ absolut
  logseq.order-list-type:: number
- Wenn $w\coloneqq \operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}>1$, dann divergiert $\sum_{k=1}^{\infty}a_{k}$
  logseq.order-list-type:: number
- Beweis
  collapsed:: true
	- absolute Konvergenz
	  logseq.order-list-type:: number
		- $b\coloneqq \frac{w+1}{2}$, also zwischen w und 1
		- somit sind fast alle $w_{k}\coloneqq \sqrt[k]{\left|a_{k}\right|};w_{k}\in\left(0,\frac{w+1}{2}\right)$
			- nur wenige nach $\frac{w+1}{2}$
		- => es gibt ein $n\in\mathbb{N}$ mit $\forall k\geq n:\sqrt[k]{\left|a_{k}\right|}\leq b<1$
		- $\Leftrightarrow\sum_{k=n}^{\infty}b^{k}$ ist eine konvergente Majorante vom $\sum_{k=n}^{\infty}\left|a_{k}\right|$
	- divergenz
	  logseq.order-list-type:: number
		- $b\coloneqq \frac{w+1}{2}>1$, also also zwischen 1 und w
		- innerhalb von $\left(w-\left(\frac{w+1}{2}\right),\infty\right)$ liegen unendlich viele $w_{k}\coloneqq \sqrt[k]{\left|a_{k}\right|}$
		- => für unendlich viele $k\in\mathbb{N}$ lief $\sqrt[k]{\left|a_{k}\right|}\geq1$
		- => $\left|a_{k}\right|\geq1$
		- => $\left(a_{k}\right)$ ist keine Nullfolge
		- $\sum_{k=1}^{\infty}a_{k}$ divergiert
- Bemerkung
	- $$\operatorname*{\mathrm{liminf}}_{k\rightarrow\infty}\frac{a_{k+1}}{a_{k}}\leq\operatorname*{\mathrm{liminf}}_{k\rightarrow\infty}\sqrt[k]{a_{k}}\leq\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{a_{k}}\leq\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\frac{a_{k+1}}{a_{k}}$$
	- => WK ist besser als QK
-
- Beispiel: Schwankende Ableitungen
	- reference:: 4.19
	- sei $\left(a_{k}\right)\subseteq\mathbb{R}$
	- $\left(a_{k}\right)=\left(\frac{1}{3^1},\frac{1}{2^2},\frac{1}{3^3},\frac{1}{2^4},\frac{1}{3^5},\frac{1}{2^6},...\right)$
	- $$a_{k}\coloneqq \left\lbrace_{\frac{1}{2^{k}}\text{, k gerade}}^{\frac{1}{3^{k}}\text{, k ungerade}}\right.$$
	- QK:
		- $$\frac{a_{k+1}}{a_{k}}=^{\text{k ungerade}}\frac{3^{k}}{2^{k+1}}=\frac12\left(\frac32\right)^{k}\longrightarrow{}_{k\rightarrow\infty}\infty$$
		- $$\frac{a_{k+1}}{a_{k}}=^{\text{k gerade}}\frac{2^{k}}{3^{k+1}}=\frac13\cdot\left(\frac23\right)^{k}\longrightarrow{}_{k\rightarrow\infty}0$$
		- Also $Q>1,q<1$, also keine Aussage
	- WK:
		- $$w_{k}=\sqrt[k]{\left|a_{k}\right|}=\left\lbrace_{\sqrt[k]{\frac{1}{2^{k}}}=\frac12\text{, k gerade}}^{\sqrt[k]{\frac{1}{3^{k}}}=\frac13\text{, k ungerade}}\right.$$
		- $$\left(w_{k}\right)=\left(\frac13,\frac12,\frac13,\frac12,...\right)$$
		- $$\Rightarrow\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}w_{k}=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}=\frac12<1$$
		- => Die Reihe $\sum_{k=1}^{\infty}a_{k}$ konvergiert absolut
-