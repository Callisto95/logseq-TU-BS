reference:: 3.14

- Eine Folge $\left(a_{k}\right)\subseteq\mathbb{R}$ heißt Cauchy-Folge (bzw. *Fundamentalfolge*), wenn $\forall\epsilon>0:\exists n\in\mathbb{N}:\forall k,l\geq n:\left|a_{k}-a_{l}\right|<\epsilon$
	- $$\Leftrightarrow\forall\epsilon>0:\exists s\in\mathbb{R}:\forall k,l\in\mathbb{N}:\left(k\geq l\geq s\Rightarrow\left|a_{k}-a_{l}\right|<\epsilon\right)$$
	- ! Es reicht **nicht** $a_{n}$ und $a_{n+1}$ bzw. $a_{k}$ und $a_{k+1}$ zu vergleichen
		- $$a_{k}:=\sum_{j=1}^{k}\frac{1}{j}=1+\frac12+...+\frac{1}{k}$$
		- $$\rightarrow a_{k+1}-a_{k}=\lim_{k\rightarrow\infty}\frac{1}{k+1}=0$$
		- aber:
		- $$\sum^{2^{n}}$$
-