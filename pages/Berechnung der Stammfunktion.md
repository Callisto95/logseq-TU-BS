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
	  collapsed:: true
		- $$I\coloneqq\varphi\left(\left\lbrack a,b\right\rbrack\right),F:I\rightarrow\mathbb{R},F\left(z\right)\coloneqq\int_{\varphi\left(a\right)}^{z}f\left(y\right)dy$$
		- $$\Rightarrow^{\text{Hauptsatz}}F^{\prime}\left(z\right)=\frac{d}{dt}\int_{\varphi\left(a\right)}^{z}f\left(y\right)dy=f\left(z\right)$$
		- $$G:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},G\left(x\right)\coloneqq F\left(\varphi\left(x\right)\right)$$
		- Kettenregel
		- $$\Rightarrow\frac{d}{dx}G\left(x\right)=\frac{d}{dx}F\left(\varphi\left(x\right)\right)=F^{\prime}\left(\varphi\left(x\right)\right)\cdot\frac{d\varphi\left(x\right)}{dx}=f\left(\varphi\left(x\right)\right)\cdot\frac{d\varphi\left(x\right)}{dx}$$
		- => G ist eine Stammfunktion von $g:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},f\left(x\right)\coloneqq f\left(\varphi\left(x\right)\right)\cdot\varphi^{\prime}\left(x\right)$
		- [Korollar 11.5]
		- $$\Rightarrow\int_{a}^{b}f\left(\varphi\left(x\right)\right)\cdot\varphi^{\prime}\left(x\right)dx=\int_{a}^{b}g\left(x\right)dx=\left\lbrack G\left(x\right)\right\rbrack_{a}^{b}=\left\lbrack F\left(\varphi\left(x\right)\right)\right\rbrack_{a}^{b}$$
		- $$=F\left(\varphi\left(b\right)\right)-F\left(\varphi\left(a\right)\right)_{}=\left\lbrack F\left(y\right)\right\rbrack_{\varphi\left(a\right)}^{\varphi\left(b\right)}=\int_{\varphi\left(a\right)}^{\varphi\left(b\right)}f\left(y\right)dy$$
-
- Erinnerung: $\frac{d}{dx}\left(f\left(x\right)g\left(x\right)\right)=f^{\prime}\left(x\right)g\left(x\right)+f\left(x\right)g^{\prime}\left(x\right)$
- Satz: **partielle Integration**
	- reference:: 11.9
	- $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$ in [a,b] stetig differentierbar
	- $$\Rightarrow\int_{a}^{b}f^{\prime}\left(x\right)g\left(x\right)dx=\left\lbrack f\left(x\right)g\left(x\right)\right\rbrack_{a}^{b}-\int_{a}^{b}f\left(x\right)g^{\prime}\left(x\right)dx$$
	- Beweis
	  collapsed:: true
		- Produktregel
		- $$\Rightarrow\left(fg\right)^{\prime}=f^{\prime}g+fg^{\prime}$$
		- $$\int_{a}^{b}\frac{d}{dx}\left(f\left(x\right)g\left(x\right)\right)dx=\int_{a}^{b}f^{\prime}\left(x\right)g\left(x\right)dx+\int_{a}^{b}f\left(x\right)g^{\prime}\left(x\right)dx$$
		- $$\int_{a}^{b}\frac{d}{dx}\left(f\left(x\right)g\left(x\right)\right)dx=\left\lbrack f\left(x\right)g\left(x\right)\right\rbrack_{a}^{b}$$
-
- Übung:
	- reference:: 11.10
	- logseq.order-list-type:: number
	  $$\int_0^1xe^{2x}dx$$
		-