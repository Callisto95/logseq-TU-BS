reference:: 8a

- Definition:
	- reference:: 8.1
	- Für $D\subseteq\mathbb{R}$ heißt $x\in D$ ein *innerer Punkt* von D, wenn es ein $\varepsilon>0$ gibt mit $\mathbb{B}_{e}\left(x\right)\subseteq D$
		- = x ist kein Randpunkt
	- dabei $D^{\circ}\coloneqq$ Menge der inneren Punkte
		- = *offenes Innere* von D
-
- Definition:
	- reference:: 8.2
	- sei $f:\mathbb{R}\rightarrowtail\mathbb{R},x\in\left(\text{Dom}f\right)^{\circ}$
	- f heißt differenzierbar, wenn der Grenzwert
	- $$f^{\prime}\left(x\right)\coloneqq\frac{d}{dx}f\left(x\right)\coloneqq\lim_{h\rightarrow0}\frac{f\left(x+h\right)-f\left(x\right)}{h}=\lim_{\xi\rightarrow x}\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}$$
		- dabei
			- $\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}$ = Steigung einer Sekante, auch $\frac{\Delta y}{\Delta x}$
			- $\frac{d}{dx}f\left(x\right)$: *Differentialquotient*, auch $\frac{d}{dx}f\left(x\right)=\frac{df\left(x\right)}{dx}=\frac{dx}{dy}$
	- existiert
	- <text>