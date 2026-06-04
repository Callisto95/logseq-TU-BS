- seien $\sum_{k=0}^{\infty}a_{k},\sum_{k=0}^{\infty}b_{k}$ absolut konvergent
- sei $m\coloneqq k+l$
- $$\sum_{m=0}^{\infty}\sum_{k=0}^{m}a_{k}b_{m-k}=\sum_{k=0}^{\infty}a_{k}\cdot\sum_{l=0}^{\infty}b_{l}$$
  konvergiert auch absolut
-
- Beweis
	- sei $\varepsilon>0$
	  $$0\neq A\coloneqq\sum_{k=0}^{\infty}\left|a_{k}\right|<\infty,0\neq B\coloneqq\sum_{k=0}^{\infty}\left|b_{k}\right|<\infty$$
	- Durch [[cauchy]]: Es gibt ein $N\in\mathbb{N}$ mit
	  $$\sum_{k=N}^{\infty}\left|a_{k}\right|<\frac{\varepsilon}{2B},\sum_{k=N}^{\infty}\left|b_{k}\right|<\frac{\varepsilon}{2A}$$
	- $$R_{n}\coloneqq\left|\sum_{m=0}^{n}\sum_{k=0}^{m}a_{k}b_{m-k}-\sum_{k=0}^{n}a_{k}\cdot\sum_{l=0}^{n}b_{k}\right|$$
	- für $n\geq2N$:
		- linker Teil: alle Produkte mit $k+l\leq n$
		  => es bleiben $k+l>n\geq2N$, also $k>N\lor l>N$
		  $$\Rightarrow R_{n}\leq\sum_{k=N}^{n}\left|a_{k}\right|\cdot\sum_{l=0}^{n}\left|b_{k}\right|+\sum_{k=0}^{n}\left|a_{k}\right|\cdot\sum_{l=N}^{n}\left|b_{l}\right|<\frac{\varepsilon}{2B}\cdot B+A\cdot\frac{\varepsilon}{2A}=\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
	- $$\exp z=\sum_{k=0}^{\infty}\frac{z^{k}}{k!},\exp0=1,\exp1=\sum_{k=0}^{\infty}\frac{1}{k!}>2$$
-
- ---
-
- # [[cauchy]] Produkt von Reihen
	- reference:: 6.9
	- $\left(a_{k}\right),\left(b_{k}\right)\subseteq\mathbb{C}$
	- $\sum_{k=0}^{\infty}a_{k},\sum_{k=0}^{\infty}b_{k}$ konvergieren absolut
	- $\begin{pmatrix}a_0b_0 & a_0b_1 & ... & a_0b_{n}\\ a_1b_0 & a_1b_1 & ... & a_1b_{n}\\ \vdots & \vdots &  & \vdots\\ a_{n}b_0 & a_{n}b_1 & ... & a_{n}b_{n}\end{pmatrix}$
	- also $\sum_{k=0}^{\infty}a_{k}\cdot\sum_{k=0}^{\infty}b_{k}\longrightarrow{}_{n\rightarrow\infty}\sum_{k=0}^{\infty}a_{k}\cdot\sum_{k=0}^{\infty}b_{k}$
	- Behauptung
		- $$\left(\sum_{k=0}^{\infty}a_{k}\right)\cdot\left(\sum_{l=0}^{\infty}b_{l}\right)=\sum_{m=0}^{\infty}\left(\sum_{k=0}^{m}a_{k}\cdot b_{m-k}\right)$$ konvergiert absolut
	- Beweis
		- $A\coloneqq\sum_{k=0}^{\infty}\left|a_{k}\right|,B\coloneqq\sum_{k=0}^{\infty}\left|b_{k}\right|$
		- o.B.d.A.: $A\neq0,B\neq0$
		- sei $\varepsilon>0$
		- Wähle $N\in\mathbb{N}$ so, dass $\sum_{k=N}^{\infty}\left|a_{k}\right|<\frac{\varepsilon}{2B},\sum_{k=N}^{\infty}\left|b_{k}\right|<\frac{\varepsilon}{2A}$
			- cauchy: $s_{M}-s_{N-1}=\sum_{_{k=N}}^{M}\left|a_{k}\right|<\varepsilon$
		- $$R_{n}\coloneqq\left|\sum_{m=0}^{n}\sum_{k=0}^{m}a_{k}b_{m-k}-\sum_{k=0}^{n}a_{k}\cdot\sum_{l=0}^{n}b_{l}\right|$$
		- Wähle $n\geq2N$, sodass $k+l\geq2N$ => $k>N\lor l>N$
		- $$\Rightarrow R_{n}\leq\sum_{k=N}^{n}\left|a_{n}\right|\cdot\sum_{l=0}^{n}\left|b_{l}\right|+\sum_{k=0}^{n}\left|a_{k}\right|\cdot\sum_{l=N}^{n}\left|b_{l}\right|<\frac{\varepsilon}{2B}\cdot B+A\cdot\frac{\varepsilon}{2A}=\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
		- => $\lim_{n\rightarrow\infty}R_{n}=0$
		- => $\left(\sum_{m=0}^{n}c_{m}\right)_{n=0}^{\infty}$ mit $c_{m}=\sum_{k=0}^{m}a_{k}b_{m-k}$ konvergiert
		- Limes: $\sum_{m=0}^{\infty}\sum_{k=0}^{m}a_{k}b_{m-k}=\left(\sum_{k=0}^{\infty}a_{k}\right)\cdot\left(\sum_{l=0}^{\infty}b_{l}\right)$
		- zur absoluten Konvergenz
			- $\sum_{m=0}^{\infty}c_{m}$ mit $c_{m}\coloneqq\sum_{k=0}^{\infty}a_{k}b_{m-k}$
			- zZ: $\sum_{m=0}^{\infty}\left|c_{m}\right|$ konvergiert
			- Beobachte: $\left|c_{m}\right|=\left|\sum_{k=0}^{m}a_{k}b_{m-k}\right|\leq\sum_{k=0}^{m}\left|a_{k}\right|\cdot\left|b_{m-k}\right|$
			- ...