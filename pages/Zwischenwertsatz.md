reference:: 7.1

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
		- $\forall k\in\mathbb{N}_0:\text{diam}I_{k}=b_{k}-a_{k}=2^{-k}\left(b-a\right)$
		  logseq.order-list-type:: number
	- Anfang: $I_0\coloneqq\left\lbrack a,b\right\rbrack$
	- Schritt: Seien für $k\in\mathbb{N}_0$ die Intervalle $\left\lbrack a_0,b_0\right\rbrack\supseteq...\supseteq\left\lbrack a_{k},b_{k}\right\rbrack$ bereits konstruiert
	- Halbiere $I_{k}:z_{k+1}\coloneqq\frac{a_{k}+b_{k}}{2}$
		- $z_{i}$ Zerlgegunspunkte
	- Auswertung von $f\left(z_{k+1}\right)$:
		- Falls $f\left(z_{k+1}\right)\geq y:a_{k+1}\coloneqq a_{k},b_{k+1}\coloneqq z_{k+1}$
		- Falls $f\left(z_{k+1}\right)<y:a_{k+1}\coloneqq z_{k+1},b_{k+1}\coloneqq b_{k}$
	- => $f\left(a_{k+1}\right)\leq y\leq f\left(b_{k+1}\right)$
	- Intervallschachtelungsprinzip (3.12):
		- $\exists\xi\in\left\lbrack a,b\right\rbrack:a_{k},b_{k}\longrightarrow{}_{k\rightarrow\infty}\xi;\forall k:\xi\in\left\lbrack a_{k},b_{k}\right\rbrack$
	- f stetig:
		- $f\left(\xi\right)=f\left(\lim_{k\rightarrow\infty}a_{k}\right)=\lim_{k\rightarrow\infty}f\left(a_{k}\right)$
		- mit $f\left(a_{k}\right)\leq y$ => $f\left(\xi\right)\leq y$
		- ---
		- $f\left(\xi\right)=f\left(\lim_{k\rightarrow\infty}b_{k}\right)=\lim_{k\rightarrow\infty}f\left(b_{k}\right)$
		- mit $f\left(b_{k}\right)\geq y\Rightarrow f\left(\xi\right)\geq y$
		-
		- => $f\left(\xi\right)=y$
-
- Übung
	- reference:: 7.2
	- $\exists w\in\mathbb{R}:w^2=2$
	  logseq.order-list-type:: number
	- Verfahren für Approximation?
	  logseq.order-list-type:: number
	- Betrachte die Funktion $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq x^2$ auf $I\coloneqq\left\lbrack0,2\right\rbrack$
	- Voraussetzungen
		- f stetig
		- $f\left(0\right)=0<2,f\left(2\right)=4>2$
		- $\Rightarrow\exists w\in\left\lbrack0,2\right\rbrack:w^2=f\left(w\right)=2$
	- Verfahren: Intervallhalbierung
		- Rekursiv: $\left(a_{n}\right),\left(b_{n}\right),\left(w_{n}\right)_{n=0}^{\infty}$
		- Start: $a_0\coloneqq0,b_0\coloneqq2,w_0\coloneqq\frac{2-0}{2}=1$
		- Schritt:
			- Falls $f\left(w_{n-1}\right)=w_{n-1}^2\leq2\Rightarrow a_{n}\coloneqq w_{n-1},b_{n}\coloneqq b_{n-1},w_{n}\coloneqq\frac{a_{n}+b_{n}}{2}$
			- Falls $f\left(w_{n-1}\right)=w_{n-1}^2>2\Rightarrow a_{n}\coloneqq a_{n-1},b_{n}\coloneqq w_{n-1},w_{n}\coloneqq\frac{a_{n}+b_{n}}{2}$
		- Fehlerabschätzung
			- $\left|w_{n}-w\right|\leq b_{n}-a_{n}=\frac{2}{2^{n}}$
-
- Satz: **Eindeutigkeit der Nullstelle**
	- reference:: 7.3
	- Die Funktion $\cos\mathbb{R}\rightarrow\mathbb{R}$ besitzt im Intervall $\left\lbrack0,2\right\rbrack$ genau eine Nullstelle
	- ?: $\cos0=1,\cos2<0\Rightarrow\cos\frac{\pi}{2}=0$
	- Idee
		- Zwischenwertatz => Nullstelle existiert
		- Monotonie auf [0,2] => Eindeutigkeit der Nullstelle
	- Beweis
		- Ziel: $\cos2<0$
			- $\cos x=\sum_{k=0}^{\infty}\left(-1\right)^{k}\frac{x^{2k}}{\left(2k\right)!}=1-\frac{x^2}{2}+r\left(x\right)$
			- mit "Rest" $r\left(x\right)\coloneqq\sum_{k=2}^{\infty}\left(-1\right)^{k}\frac{x^{2k}}{\left(2k\right)!}$
			-