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