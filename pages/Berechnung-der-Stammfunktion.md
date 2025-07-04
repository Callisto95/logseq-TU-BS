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
  collapsed:: true
	- reference:: 11.10
	- logseq.order-list-type:: number
	  $$\int_0^1xe^{2x}dx$$
		- mit $x\rightarrow f\left(x\right),e^{2x}=g^{\prime}\left(x\right)$
		- $$=^{\text{p.I.}}\left\lbrack\left\lbrack x\right\rbrack_{f\left(x\right)}\cdot\left\lbrack\frac12e^{2x}\right\rbrack_{g\left(x\right)}\right\rbrack_0^1-\int_0^11\cdot\frac12e^{2x}dx$$
		- $$=\frac12e^2-0-\left\lbrack\frac14e^{2x}\right\rbrack_1^0$$
		- $$=\frac12e^2-\left(\frac{e^2}{4}-\frac14\right)=\frac{e^2}{4}+\frac14$$
	- logseq.order-list-type:: number
	  $$\int_2^3\ln\left(x\right)dx=\int_2^3\left\lbrack1\right\rbrack_{f^{\prime}\left(x\right)}\cdot\left\lbrack\ln\left(x\right)\right\rbrack_{g\left(x\right)}dx$$
		- $$=^{\text{p.I.}}\left\lbrack\left\lbrack x\right\rbrack_{f\left(x\right)}\cdot\left\lbrack\ln x\right\rbrack_{g\left(x\right)}\right\rbrack_2^3-\int_2^3\left\lbrack x\right\rbrack_{f\left(x\right)}\cdot\left\lbrack\frac{1}{x}dx\right\rbrack_{g^{\prime}\left(x\right)}dx=\left\lbrack x\cdot\ln x-x\right\rbrack_2^3$$
		- $$=3\ln3-2\ln2-1$$
		- $$=\ln3^3-\ln2^2-1=\ln\frac{27}{4}-1$$
		- Alternativ
			- $$\int\ln\left(x\right)dx=\int\ln\left(x\right)\cdot x\cdot\frac{1}{x}\left\lbrack dx\right\rbrack_{dy}$$
				- = als: $y\coloneqq\varphi\left(x\right)=\ln x,\frac{dy}{dx}=\varphi^{\prime}\left(x\right)=\frac{1}{x}$
			- $$=\left\lbrack\int y\cdot e^{y}dy\right\rbrack_{y=\ln x}$$
			- und
			- $$\int\left\lbrack y\right\rbrack_{f\left(y\right)}\cdot\left\lbrack e^{x}\right\rbrack_{g^{\prime}\left(x\right)}dx=y\cdot e^{y}-\int1\cdot e^{y}dy=y\cdot e^{y}-e^{y}=\int\ln\left(x\right)dx=\ln x\cdot x-x$$
	- logseq.order-list-type:: number
	  $$\int\left\lbrack e^{x}\right\rbrack_{f^{\prime}\left(x\right)}\cdot\left\lbrack\sin x\right\rbrack_{g\left(x\right)}dx$$
		- $$=^{\text{p.I.}}\left\lbrack e^{x}\right\rbrack_{f\left(x\right)}\cdot\left\lbrack\sin x\right\rbrack_{g\left(x\right)}-\int\left\lbrack e^{x}\right\rbrack_{u^{\prime}\left(x\right)}\cdot\left\lbrack\cos\left(x\right)\right\rbrack_{v\left(x\right)}dx$$
		- $$=^{\text{p.I.}}e^{x}\cdot\sin x-\left(\left\lbrack e^{x}\right\rbrack_{u\left(x\right)}\cdot\left\lbrack\cos x\right\rbrack_{v\left(x\right)}-\int\left\lbrack e^{x}\right\rbrack_{u\left(x\right)}\cdot\left\lbrack-\sin x\right\rbrack_{v^{\prime}\left(x\right)}dx\right)$$
		- $$\Rightarrow2\cdot\int e^{x}\sin\left(x\right)dx=e^{x}\sin x-e^{x}\cos x=e^{x}\left(\sin x-\cos x\right)$$
	- logseq.order-list-type:: number
	  $$\int\left\lbrack\frac{1}{t}\right\rbrack_{\varphi^{\prime}\left(t\right)}\left\lbrack\ln\left(t\right)\right\rbrack_{\varphi\left(t\right)}dt$$
		- $$=\int\left\lbrack\varphi^{\prime}\left(t\right)\right\rbrack_1\cdot\left\lbrack\varphi\left(t\right)\right\rbrack_{y}\left\lbrack dt\right\rbrack_2$$
			- $$1\&2:dy=\varphi^{\prime}\left(t\right)dt$$
		- $$=\left\lbrack\int y\space dy\right\rbrack_{y=\ln t}=\left\lbrack\frac12y^2\right\rbrack_{y=\ln t}=\frac12\ln^2t$$
	- logseq.order-list-type:: number
	  $$\int_0^4\sqrt{1+\sqrt{x}}dx$$
		- $$y=\varphi\left(x\right)\coloneqq\sqrt{x},\frac{dy}{dx}=\varphi^{\prime}\left(x\right)=\frac12\frac{1}{\sqrt{x}},dy=\frac12\frac{1}{\sqrt{x}}dx$$
		- $$=\int_0^4\left\lbrack\sqrt{1+\sqrt{x}}\right\rbrack_{\sqrt{1+y}}\cdot\left\lbrack2\sqrt{x}\right\rbrack_{2y}\cdot\left\lbrack\frac12\frac{1}{\sqrt{x}}dx\right\rbrack_{dy}$$
		- $$=\int_0^2\left\lbrack\sqrt{1+y}\right\rbrack_{f^{\prime}\left(x\right)}\cdot\left\lbrack2y\right\rbrack_{g\left(x\right)}dy$$
		- $$f^{\prime}\left(y\right)=\sqrt{1+y}=\left(1+y\right)^{\frac12}\Rightarrow f\left(y\right)=\frac23\left(1+y\right)^{\frac32}$$
		- $$=^{\text{p.I.}}\left\lbrack\frac23\left(1+y\right)^{\frac32}\cdot2y\right\rbrack_0^2-\int_0^2\left\lbrack\frac23\left(1+y\right)^{\frac32}\right\rbrack_{f\left(y\right)}\cdot\left\lbrack2\right\rbrack_{g^{\prime}\left(y\right)}\space dy$$
		- $$=\frac83\cdot3^{\frac32}-\left\lbrack\frac43\cdot\frac25\left(1+y\right)^{\frac52}\right\rbrack_0^2=\frac{8}{15}\left(6\sqrt3+1\right)$$
	- logseq.order-list-type:: number
	  $$\int_0^1\sqrt{1-x^2}dx$$
		- Substitution: $x\coloneqq\sin t,t\coloneqq\arcsin x$
		- $$\frac{dx}{dt}=\cos t\Rightarrow dx=\cos\left(t\right)dt$$
		- $$\rightarrow\int_0^1\left\lbrack\sqrt{1-x^2}\right\rbrack_{\sqrt{1-\sin^2t}}\left\lbrack dx\right\rbrack_{\cos\left(t\right)dt}=\int_{t=0}^{t=\frac{\pi}{2}}\sqrt{1-\sin^2t}\cos\left(t\right)dt$$
			- $$\cos^2t+\sin^2t=1\Leftrightarrow1-\sin^2t=\cos^2t,\cos t\geq0$$
		- $$=\int_0^{\frac{\pi}{2}}\left\lbrack\cos t\right\rbrack_{u\left(t\right)}\cdot\left\lbrack\cos t\right\rbrack_{v^{\prime}\left(t\right)}\space dt$$
		- $$=^{\text{p.I.}}\left\lbrack\left\lbrack\cos t\right\rbrack_{u\left(t\right)}\cdot\left\lbrack\sin t\right\rbrack_{v\left(t\right)}\right\rbrack_0^{\frac{\pi}{2}}-\int_0^{\frac{\pi}{2}}\left\lbrack\left(-\sin t\right)\right\rbrack_{u^{\prime}\left(t\right)}\cdot\left\lbrack\sin t\right\rbrack_{v\left(t\right)}\space dt$$
		- $$=\int_0^{\frac{\pi}{2}}\sin^2t\space dt$$
		- $$\int_0^1\sqrt{1-x^2}dx=\int_0^{\frac{\pi}{2}}\cos^2t\space dt=\int_0^{\frac{\pi}{2}}\left\lbrack\sin^2t\right\rbrack_{1-\cos^2t}\space dt$$
		- $$=\int_0^{\frac{\pi}{2}}1dt-\int_0^{\frac{\pi}{2}}\cos^2t\space dt$$
		- $$\Rightarrow2\cdot\int_0^{\frac{\pi}{2}}\cos^2t\space dt=\int_0^{\frac{\pi}{2}}1dt=\frac{\pi}{2}$$
		- $$\Rightarrow\int_0^1\sqrt{1-x^2}dx=\frac{\pi}{4}$$
-