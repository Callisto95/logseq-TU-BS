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
-