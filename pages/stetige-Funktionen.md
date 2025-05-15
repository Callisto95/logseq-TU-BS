- sei $f:\mathbb{R}\rightarrow\mathbb{R}$
	- Input x -> Output f(x)
- Probleme
	- x Fehlerbefreit?
	- Was passiert mit f(x)?
	- genauigkeit bei $x=\sqrt2,x=\pi$: "Exakte Eingabe"
- Möchte: Wenn $x\approx y\Rightarrow f\left(x\right)\approx f\left(y\right)$
-
- Definition: **Stetigkeit**
	- reference:: 5.a
	- sei $f:\mathbb{R}\rightarrow\mathbb{R}$ eine (partielle) Funktion
	- d.h. $D:=\text{Dom}f\subseteq\mathbb{R}$ und $f:D\rightarrow\mathbb{R}$
	- für $v\in D$ heißt f *stetig in v*, wenn $\forall\epsilon>0:\exists\delta>0:\forall x\in D:\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|<\epsilon$
	  logseq.order-list-type:: number
		- $\epsilon>0$: Fehler im Output (y-Ball / y-Variation)
		- $\delta>0$: ausreichende Präzision im Input (x-Ball / x-Variation)
	- Wenn f in jedem $v\in D$ stetig ist, dann heißt stetig (f ist eine stetige Funktion)
	  logseq.order-list-type:: number
		- $f\in C\left(D\right)$, f aus der Klasse der stetigen Funktionen (C: continous)
	- Beispiel
		- $f:\mathbb{R}\rightarrow\mathbb{R}:f\left(x\right)=42$
		  logseq.order-list-type:: number
			- sei $\epsilon>0$, jedes $\delta>0$ erfüllt Stetigkeit
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)=x$
		  logseq.order-list-type:: number
			- zu $\epsilon>0$ wähle $\delta:=\epsilon$
			- $$\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|=\left|x-v\right|<\delta=e$$
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right):=2x$
		  logseq.order-list-type:: number
			- zu $\epsilon>0$ wähle $\delta:=\frac{\epsilon}{2}$
			- $\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|=\left|2x-2v\right|=2\left|x-v\right|<2\cdot\delta=2\cdot\frac{\epsilon}{2}=\epsilon$
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)=x^2$
		  logseq.order-list-type:: number
			- Stetigkeit in $v\in\mathbb{R}:x=v+h$
			- Ziel: $\left|f\left(v\right)-f\left(v+h\right)\right|<\epsilon$
				- $=\left|v^2-\left(v+h\right)^2\right|=\left|2vh-h^2\right|=\left|h\right|\cdot\left|2v+h\right|\Rightarrow\left\lbrack<\delta\right\rbrack\cdot\left\lbrack<^{?}\epsilon\right\rbrack$
			- Idee
				- $\left|2v+h\right|\cdot\delta<\epsilon\Rightarrow\delta=\frac{\epsilon}{\left|2v+h\right|}$
				- Notiz: $\left|2v+h\right|\leq\left|2v\right|+\left|h\right|\leq^{\left|h\right|\leq1}2\left|v\right|+1$
				- Wähle $\delta=\delta\left(v,\epsilon\right):=\min\left\lbrace\frac{1}{2\left|v\right|+1}\epsilon,1\right\rbrace$