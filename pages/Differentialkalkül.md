reference:: 11

- auch *Integration und Differentiation*
-
- **Hauptsatz**
	- reference:: 11a
	- idk
-
- Satz: **Integralfunktion**
	- reference:: 11.1
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack$ ist die Integralfunktion $I:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},x\mapsto I\left(x\right)\coloneqq\int_{a}^{x}f\left(t\right)dt$
	- ist lipschitz mit Konstanten
	- $$\sup_{t\in\left\lbrack a,b\right\rbrack}\left|f\left(t\right)\right|$$
	- d.h.
	- $$\forall x,y\in\left\lbrack a,b\right\rbrack:\left|\left\lbrack\int_{a}^{x}f\left(t\right)dt\right\rbrack_{I\left(x\right)}-\left\lbrack\int_{a}^{y}f\left(t\right)dt\right\rbrack_{I\left(y\right)}\right|\leq\left\lbrack\sup_{t\in\left\lbrack a,b\right\rbrack}\left|f\left(t\right)\right|\right\rbrack_{=L}\cdot\left|x-y\right|$$
	- Beweis
		- für $y<x$ gilt
		- $$\int_{a}^{x}f\left(t\right)dt=\int_{a}^{y}f\left(t\right)dt+\int_{a}^{x}f\left(t\right)dt$$
		- $$\Rightarrow\int_{a}^{x}f\left(t\right)dt-\int_{a}^{y}f\left(t\right)dt=\int_{y}^{x}f\left(t\right)dt$$
		- $$\Rightarrow\left|\int_{a}^{x}f\left(t\right)dt-\int_{a}^{y}f\left(t\right)dt\right|=\left|\int_{y}^{x}f\left(t\right)dt\right|\leq\int_{y}^{x}\left|f\left(t\right)\right|dt\leq L\cdot\int_{y}^{x}1dt=L\cdot\left(x-y\right)$$
-
- Vereinbarung:
	- reference:: 11.2
	- $f\in\mathbb{R}\left\lbrack a,b\right\rbrack,c\in\left\lbrack a,b\right\rbrack$
	- $$\int_{b}^{a}f\left(t\right)dt\coloneqq-\int_{a}^{b}f\left(t\right)dt$$
	- $$\int_{c}^{c}f\left(t\right)dt\coloneqq0$$
-
- Defintion: **Stammfunktion**
	- reference:: 11.3
	- $D=D^{\circ}\subseteq\mathbb{R}$ offene Menge, $f:D\rightarrow\mathbb{R}$
	- Dann heißt $F:D\rightarrow\mathbb{R}$ heißt eine Stammfunktion von f, wenn F differentierbar ist mit F'=f
-
- Theorem: **Hauptsatz des Differentialkalküls**
	- reference:: 11.4
	- sei $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ stetig
	- Die Integralfunktion $\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},x\mapsto\int_{a}^{x}f\left(t\right)dt$ ist im Intervall (a,b) differentierbar, und dort gilt $\frac{d}{dx}\int_{a}^{x}f\left(t\right)dt=f\left(x\right)$
	  logseq.order-list-type:: number
	- Wenn $F:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ stetig ist, außerdem in (a,b) differentierbar mit F'(x)=f(x), dann gilt $F\left(x\right)=F\left(a\right)+\int_{a}^{x}f\left(t\right)dt$
	  logseq.order-list-type:: number
		- bzw. $F\left(x\right)-F\left(a\right)=\int_{a}^{x}f\left(t\right)dt$
	- Beweise
		- für $x\in\left(a,b\right)$ ist zZ:
		  logseq.order-list-type:: number
			- $$\frac{d}{dx}\int_{a}^{x}f\left(t\right)dt=\lim_{h\rightarrow0}\frac{1}{h}\cdot\left(\int_{a}^{x+h}f\left(t\right)dt-\int_{a}^{x}f\left(t\right)dt\right)=_{\text{zZ}}f\left(x\right)$$
			- für $h\neq0$ gibt es nahc dem MWS der Integralrechnung ein $\xi_{h}$ zeischen x und x+h, so dass
			- $$\int_{a}^{x+h}f\left(t\right)dt-\int_{a}^{x}f\left(t\right)dt=\int_{a}^{x}f\left(t\right)dt+\int_{x}^{x+h}f\left(t\right)dt-\int_{a}^{x}f\left(t\right)dt$$
			- $$=\int_{x}^{x+h}f\left(t\right)dt=^{MWS}f\left(\xi_{h}\right)\cdot h$$
			- $$\Rightarrow\frac{1}{h}\left(\int_{a}^{x+h}f\left(t\right)dt-\int_{a}^{x}f\left(t\right)dt\right)=\frac{1}{h}\cdot f\left(\xi_{h}\right)\cdot h\longrightarrow{}_{h\rightarrow0}f\left(x\right)$$
		- für $x\in\left(a,b\right)$ gilt
		  logseq.order-list-type:: number
			- $$F\left(x\right)-\int_{a}^{x}f\left(t\right)dt=^{\text{zZ}}F\left(a\right)$$
			- $$\frac{d}{dx}\left(F\left(x\right)-\int_{a}^{x}f\left(t\right)dt\right)=F^{\prime}\left(x\right)-$$