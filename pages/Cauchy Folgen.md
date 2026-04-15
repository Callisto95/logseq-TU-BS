reference:: 3.14
alias:: cauchy

- Eine Folge $\left(a_{k}\right)\subseteq\mathbb{R}$ heißt Cauchy-Folge (bzw. *Fundamentalfolge*), wenn
	- $$\forall\varepsilon>0:\exists n\in\mathbb{N}:\forall k,l\geq n:\left|a_{k}-a_{l}\right|<\varepsilon$$
	- $$\Leftrightarrow\forall\varepsilon>0:\exists s\in\mathbb{R}:\forall k,l\in\mathbb{N}:\left(k\geq l\geq s\Rightarrow\left|a_{k}-a_{l}\right|<\varepsilon\right)$$
	- ! Es reicht **nicht** $a_{n}$ und $a_{n+1}$ bzw. $a_{k}$ und $a_{k+1}$ zu vergleichen
	  collapsed:: true
		- $$a_{k}\coloneqq \sum_{j=1}^{k}\frac{1}{j}=1+\frac12+...+\frac{1}{k}$$
		- $$\rightarrow a_{k+1}-a_{k}=\lim_{k\rightarrow\infty}\frac{1}{k+1}=0$$
		- aber:: Übung 1.2
		- $$\sum_{j=1}^{2^{n}}\frac{1}{j}\geq\frac12\Rightarrow\left(a_{k}\right)\text{divergiert}$$
-
- Satz: konvergente Folgen sind cauchy
	- reference:: 3.15
	- Sei $\left(a_{k}\right)\subseteq\mathbb{R}$ konvergent, dann ist $\left(a_{k}\right)$ cauchy
	- Sei $\varepsilon>0$, schreibe $a\coloneqq \lim_{k\rightarrow\infty}a_{k}$
	- => es gibt ein $n=n\left(\varepsilon\right)\in\mathbb{N}$ mit $\forall k\geq n:\left|a_{k}-a\right|>\frac{\varepsilon}{2}$
	- => für $k,l\geq n$ gilt nach der Dreiecksungleichung: $\left|a_{k}-a_{l}\right|=\left|a_{k}-a+a-a_{l}\right|\leq\left|a_{k}-a\right|+\left|a-a_{l}\right|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$
-