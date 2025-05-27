reference:: 6d

- $$e^{x}=\lim_{n\rightarrow\infty}\sum_{k=0}^{n}\frac{x^{k}}{k!}=\lim_{n\rightarrow\infty}\left(1+\frac{x}{1!}+\frac{x^2}{2!}+...+\frac{x^{n}}{n!}\right)$$
- mit
  collapsed:: true
	- $f_0\left(x\right)=1$
	- $f_1\left(x\right)=x$
	- $f_2\left(x\right)=x^2$, aber verschoben nach unten links
	- => alle gehen durch Punkt $\left(0,1\right)$
-
- Definition: gleichmäßige und punktmäßige Konvergenz
	- reference:: 6.15
	- $D\subseteq\mathbb{R},\left(f_{n}\right)_{n=1}^{\infty}$ mit $f_{n}:D\rightarrow\mathbb{R}$ "Funktionsfolge"
	- punktweise Konvergenz
	  logseq.order-list-type:: number
		- $\left(f_{n}\right)$ konvergiert Punktweise gegen $f:D\rightarrow\mathbb{R}$, wenn $\forall x\in D:f_{n}\left(x\right)\longrightarrow{}_{n\rightarrow\infty}f\left(x\right)$
		- d.h.: $\forall x\in D:\forall\varepsilon>0:\exists m\in\mathbb{N}:\forall n\geq m:\left|f_{n}\left(x\right)-f\left(x\right)\right|<\varepsilon$
			- mit $m=m\left(\varepsilon,x\right)$
	- gleichmäßige Konvergenz
	  logseq.order-list-type:: number
		- $\left(f_{n}\right)$ konvergiert gleichmäßig gegen $f:D\rightarrow\mathbb{R}$, wenn
		- $\forall\varepsilon>0:\exists m\in\mathbb{N}:\forall n\geq m:\forall x\in D:\left|f_{n}\left(x\right)-f\left(x\right)\right|<\varepsilon$
			- mit $m=m\left(\varepsilon\right)\neq m\left(\varepsilon,x\right)$
			- Unterschied zu Punktkonvergenz: gilt für alle Punkte, nicht nur einer
-