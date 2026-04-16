reference:: 12a

- Wenn $f:\mathbb{R}\rightarrowtail\mathbb{R}$ in $\left(a,b\right)\subseteq\text{Dom}f\subseteq\mathbb{R}$ differentierbar ist
  collapsed:: true
	- Frage: ist $f^{\prime}:\mathbb{R}\rightarrowtail\mathbb{R}$ in $x\in\left(a,b\right)$ wieder differntierbar
	- also $f^{\prime\prime}\left(x\right)=\frac{d^2}{dx^2}f\left(x\right)=\frac{d}{dx}\left(\frac{d}{dx}f\left(x\right)\right)=\frac{d}{dx}f^{\prime}\left(x\right)$
	- $$=\lim_{\xi\rightarrow x}\frac{f^{\prime}\left(\xi\right)-f^{\prime}\left(x\right)}{\xi-x}$$
	- $$f^{\left(0\right)}\left(x\right)\coloneqq\frac{d^{\left(0\right)}}{dx^{\left(0\right)}}f\left(x\right)\coloneqq f\left(x\right)$$
		- Start; "Nullte Ableitung"
-
- Defintion: **(n+1)-te Ableitung von f**
	- reference:: 12.1
	- sei $f:\mathbb{R}\rightarrowtail\mathbb{R}$ eine Funktion, die für ein $n\in\mathbb{N}_0$ in $I=\left(a,b\right)\subseteq\text{Dom}f$ mindestenz n-Mal differentierbar ist
	- Wenn für $x\in I$ die n-te Ableitung $f^{\left(n\right)}:\mathbb{R}\rightarrowtail\mathbb{R}$ in x differentierbar ist, heißt
		- $$f^{\left(n+1\right)}\left(x\right)=\frac{d^{n+1}}{dx^{n+1}}f\left(x\right)\coloneqq\frac{d}{dx}f^{\left(n\right)}\left(x\right)=\lim_{\xi\rightarrow x}\frac{f^{\left(n\right)}\left(\xi\right)-f^{\left(n\right)}\left(x\right)}{\xi-x}$$
-
- Definition: **n-malige stetige Differentierbarkeit**
	- reference:: 12.2
	- Wenn $f:\mathbb{R}\rightarrow\mathbb{R}$ in $M\subseteq\left(\text{Dom}f\right)^{\circ}$ wenigsten n-Mal differentierbar ist und $f^{\left(n\right)}$ in M stetig ist, heißt f in M n-Mal stetig differentierbar: $f\in C^{n}\left(M\right)$
	- Wenn $f\in C^{n}\left(M\right)$ für alle $n\in\mathbb{N}_0$:
		- $f\in C^{\infty}\left(M\right)$, f ist *glatte Funktion*
-
- Beispiele
	- logseq.order-list-type:: number
	  $$m\in\mathbb{N},f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq x^{m}$$
		- $$\frac{d}{dx}x^{m}=m\cdot x^{m-1}$$
		- $$\left(\frac{d}{dx}\right)^2x^{m}=m\cdot\left(m-1\right)\cdot x^{m-2}$$
		- $\Rightarrow f\in C^{\infty}\left(\mathbb{R}\right)$ und für $n\in\left\lbrace0,...,m\right\rbrace$ gilt
			- $$\left(\frac{d}{dx}\right)^{n}x^{m}=m\cdot\left(m-1\right)\cdot...\cdot\left(m-n+1\right)\cdot x^{m-n}=\frac{m!}{\left(m-n\right)!}x^{m-n}$$
	- Die Exponentialfunktion ist glatt
	  logseq.order-list-type:: number
		- $$\forall n\in\mathbb{N}_0:\left(\frac{d}{dx}\right)^{n}e^{x}=e^{x}$$
	- [[trigonometrische-Funktionen]]
	  logseq.order-list-type:: number
		- $$\sin x\longrightarrow{}_{\frac{d}{dx}}\cos x\longrightarrow{}_{\frac{d}{dx}}-\sin x\longrightarrow{}_{\frac{d}{dx}}-\cos x\longrightarrow{}_{\frac{d}{dx}}\sin x$$
		- $$\left(\frac{d}{dx}\right)^{2n}\sin x=\left(-1\right)^{n}\sin x,\left(\frac{d}{dx}\right)^{2n-1}\sin x=\left(-1\right)^{n+1}\cos x$$
		- $$\left(\frac{d}{dx}\right)^{2n}\cos x=\left(-1\right)^{n}\cos x,\left(\frac{d}{dx}\right)^{2n-1}\cos x=\left(-1\right)^{n}\sin x$$
-