reference:: 11b

- Achtung: $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq e^{-x^2}$ hat zwar eine Stammfunktion: $x\mapsto\int_0^{x}e^{-t^2}dt$, aber es gibt keinen "elementaren Ausdruck"
-
- Beispiel
  collapsed:: true
	- $$\int\left(-2x\right)e^{-x^2}dx=e^{-x^2}=\left\lbrack\int e^{y}dy\right\rbrack_{y=-x^2}$$
-
- Korollar: **Variablensubstitution**
	- reference:: 11.8
	- $f:\mathbb{R}\rightarrowtail\mathbb{R}$ stetig, $\varphi:\mathbb{R}\rightarrowtail\mathbb{R}$ sei in $\left\lbrack a,b\right\rbrack\subseteq\left(\text{Dom}\varphi\right)^{\circ}$ stetig differenzierbar
	- Außerdem gelte $\varphi\left(\left\lbrack a,b\right\rbrack\right)\subseteq\text{Dom}f$
	- $$\rightarrow\int_{\varphi\left(b\right)}^{\varphi\left(a\right)}f\left(y\right)dy=\int_{a}^{b}f\left(\varphi\left(x\right)\right)\cdot\left\lbrack\frac{d\varphi\left(x\right)}{dx}dx\right\rbrack_{y=\varphi\left(x\right),\frac{dy}{dx}dx=dy}$$
	- Beweis
		- $$I\coloneqq\varphi\left(\left\lbrack a,b\right\rbrack\right),F:I\rightarrow\mathbb{R},F\left(z\right)\coloneqq\int_{\varphi\left(a\right)}^{z}f\left(y\right)dy$$
		- $$\Rightarrow^{\text{Hauptsatz}}F^{\prime}\left(z\right)=\frac{d}{dt}\in$$