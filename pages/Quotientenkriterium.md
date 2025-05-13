reference:: 4.14

- Es sei $\sum_{k=1}^{\infty}a_{k}\subseteq\mathbb{R}$ mit $\frac{a_{n+1}}{a_{n}}\leq b$, wobei b der Schrumpffaktor ist
	- das muss nicht sofort gelten und $\forall k:a_{k}\neq0$
- Wenn $Q:=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}<1$, dann konvergiert $\sum a_{k}$ absolut
  logseq.order-list-type:: number
	- $\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}$ ist in Relation zu $q_{k}$
- Wenn $q:=\operatorname*{\mathrm{liminf}}_{k\rightarrow\infty}\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}>1$, dann divergiert $\sum a_{k}$
  logseq.order-list-type:: number
- Wenn q<1 und Q>1, dann keine Aussage
-
- Beweis
  collapsed:: true
	- Sei Q gegeben
	- Umgebung um Q, die aber kleiner als 1 bleibt
	- in $\left(0,Q+\text{radius}\right)$ liegen fast alle $q_{k}$
	- ---
	- zu 1.
		- Es gibt einen $b<1$ (z.B. $b:=\frac{Q+1}{2}$) und ein $m\in\mathbb{N}$ mit
		- $$\forall k\geq m:q_{k}=\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}\leq b<1$$
		- $$\Rightarrow\left|a_{k+1}\right|\leq b\cdot\left|a_{k}\right|$$
		- Rekursiv: $\left|a_{k}\right|\leq b^{k-m}\left|a_{m}\right|=b^{k}\cdot\frac{\left|a_{m}\right|}{b^{m}}$
		- $$\Rightarrow\sum_{k=m}^{\infty}\left|a_{m}\right|b^{k-m}=\left|a_{m}\right|\cdot\sum_{l=0}^{\infty}b^{l}$$
		- ist eine konvergente Majorante von $\sum_{k=m}^{\infty}a_{k}$
	- zu 2.
		- in $\left(0,q-\text{radius}\right)$ liegen endlich viele $q_{k}$
		- Es gibt ein $b>1$ (z.B. $b:=\frac{1+q}{2}$) und ein Schwellenindex $m\in\mathbb{N}$ mit
		- $$\forall k\geq m:\frac{\left|a_{k+1}\right|}{\left|a_{k}\right|}\geq b>1$$
		- $$\Rightarrow\left|a_{k+1}\right|\geq\left|a_{k}\right|\geq\left|a_{m}\right|>0$$
		- => $\left(a_{k}\right)$ ist keine Nullfolge
		- => $\sum a_{k}$ divergiert
-
- Beispiel: QK zu folgenden funktionen
	- reference:: 4.17
	- $\sum\frac{1}{k}$
	  logseq.order-list-type:: number
		- $$q_{k}=\frac{\frac{1}{k+1}}{\frac{1}{k}}=\frac{k}{k+1}\longrightarrow{}_{k\rightarrow\infty}1$$
	- $\sum\frac{1}{k^2}$
	  logseq.order-list-type:: number
		- $$q_{k}=\frac{\frac{1}{\left(k+1\right)^2}}{\frac{1}{k^2}}=\frac{k^2}{\left(k+1\right)^2}=\frac{k^2}{k^2+2k+1}=\frac{1}{1+\frac{2}{k}+\frac{1}{k^2}}\longrightarrow{}_{k\rightarrow\infty}1$$
		- keine Aussage
	- $\sum_{k=1}^{\infty}\frac{k!}{k^{k}}$
	  logseq.order-list-type:: number
		- Notiere: $\frac{k!}{k^{k}}=\frac{1}{k}\cdot\frac{2}{k}\cdot...\cdot\frac{k}{k}$
			- Abschätzung: $\frac{2}{k^2}$ ~> Konvergenz
		- QK: $a_{k}:=\frac{k!}{k^{k}}\neq0$
		- $q_{k}:=\left|\frac{a_{k+1}}{a_{k}}\right|=\frac{\frac{\left(k+1\right)!}{\left(k+1\right)^{k+1}}}{\frac{k!}{k^{k}}}=\left(\frac{k}{k+1}\right)^{k}=\frac{1}{\left(\frac{k+1}{k}\right)^{k}}=\frac{1}{\left(1+\frac{1}{k}\right)^{k}}\longrightarrow{}_{k\rightarrow\infty}\frac{1}{e}$
		- Die Reihe $\sum_{k=1}^{\infty}\frac{k!}{k^{k}}$ konvergiert nach dem QK absolut, also insbesondere im gewöhnlichem Sinn
		- Konvergenz: Idee: Abschätzung durch konvergente Majorante: $\left|a_{k}\right|\leq c\cdot b^{k}$
			- => $\sqrt[k]{\left|a_{k}\right|}\leq\sqrt[k]{c}\cdot b$
-
- Satz: **Wurzelkriterium**
	- reference:: 4.18
	- Sei $\left(a_{k}\right)\subseteq\mathbb{R}$
	- Wenn $w:=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}<1$, dann konvergiert $\sum_{k=1}^{\infty}a_{k}$ absolut
	  logseq.order-list-type:: number
	- Wenn $w:=\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[k]{\left|a_{k}\right|}>1$, dann divergiert $\sum_{k=1}^{\infty}a_{k}$
	  logseq.order-list-type:: number
	- Beweis
	  collapsed:: true
		- absolute Konvergenz
		  logseq.order-list-type:: number
			- $b:=\frac{w+1}{2}$, also zwischen w und 1
			- somit sind fast alle $w_{k}:=\sqrt[k]{\left|a_{k}\right|};w_{k}\in\left(0,\frac{w+1}{2}\right)$
				- nur wenige nach $\frac{w+1}{2}$
			- => es gibt ein $n\in\mathbb{N}$ mit $\forall k\geq n:\sqrt[k]{\left|a_{k}\right|}\leq b<1$
			- $\Leftrightarrow\sum_{k=n}^{\infty}b^{k}$ ist eine konvergente Majorante vom $\sum_{k=n}^{\infty}\left|a_{k}\right|$
		- divergenz
		  logseq.order-list-type:: number
			- $b:=\frac{w+1}{2}>1$, also also zwischen 1 und w
			- innerhalb von $\left(w-\left(\frac{w+1}{2}\right),\infty\right)$ liegen unendlich viele $w_{k}:=\sqrt[k]{\left|a_{k}\right|}$
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
	- $$a_{k}:=\left\lbrace_{\frac{1}{2^{k}}\text{, k gerade}}^{\frac{1}{3^{k}}\text{, k ungerade}}\right.$$
	-
-