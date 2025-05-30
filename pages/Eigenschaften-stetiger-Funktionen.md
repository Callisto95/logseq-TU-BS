reference:: 7

- Schulweisheit: stetige Funktion kann man ohne absetzen zeichnen
	- $f:x\mapsto\frac{1}{x}$ ist aber stetig
- $$f\left(x\right)=\left\lbrace_{0,x=0}^{x\cdot\sin\frac{1}{x},x\neq0}\right.$$
- Wenn $x_{n}\longrightarrow{}_{n\rightarrow\infty}0\Rightarrow f\left(x_{n}\right)\longrightarrow{}_{n\rightarrow\infty}0\Rightarrow$f ist stetig
-
- **Zwischenwertsatz**
	- reference:: 7a
	- Konvexe Hülle: $\text{Conv}\left\lbrace x,y\right\rbrace\coloneqq\left\lbrace_{\left\lbrack y,x\right\rbrack,x>y}^{\left\lbrack x,y\right\rbrack,x\leq y}\right.$
	- = Intervall zwischen x und y
-
- **Zwischenwertsatz**
	- reference:: 7.1
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ stetig
	- $\forall y\in\text{Conv}\left\lbrace f\left(a\right),f\left(b\right)\right\rbrace:\exists\xi\in\left\lbrack a,b\right\rbrack:f\left(\xi\right)=y$
	- Anwendung:
	  collapsed:: true
		- $\sqrt2,\sqrt3$ für Computer?
		- $\sqrt2\rightsquigarrow x^2-2=0$
		- $\sqrt3\rightsquigarrow x^2-3=0$
	- Beweis:
		- Idee: Intervallhalbierung
		- Rekursive: Intervallschachtelung $\left(I_{k}\right)_{k=0}^{\infty}$ mit $I_{k}=\left\lbrack a_{k},b_{k}\right\rbrack$ und
			- $\forall k\in\mathbb{N}_0:f\left(a_{k}\right)\leq y\leq f\left(b_{k}\right)$
			  logseq.order-list-type:: number
			- $\forall k\in\mathbb{N}_0:\text{diam}I_{k}=b_{k}-a_{k}=2^{-k}\left(\right)$
			  logseq.order-list-type:: number