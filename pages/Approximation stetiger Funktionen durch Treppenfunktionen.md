reference:: 10.13

- Zu jeder stetigen Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ und jedem $\varepsilon>0$ gibt es Treppenfunktionen $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit 
  $$\varphi\leq f\leq\psi\land\psi-\varphi<\varepsilon$$
- Beweis
  collapsed:: true
	- Übung 7.15 => f ist sogar gleichmäßig stetig
	- => Es gibt ein $\delta=\delta\left(\varepsilon\right)>0\left(\delta\neq\delta\left(x\right)\right)$ mit
	  $$\forall x,y\in\left\lbrack a,b\right\rbrack:\left|x-y\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(y\right)\right|<\frac{\varepsilon}{2}$$
	- Zerlegungsstellen: für $k\in\left\lbrace0,...,n\right\rbrace$
		- $$x_{k}\coloneqq a+k\cdot\Delta x=a+k\cdot\frac{b-a}{n}$$
	- => Zerlegung $\left(x_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack a,b\right\rbrack,\Phi\left(\left(x_{k}\right)\right)=\Delta x<\delta$
	- Definiere $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ durch
		- für $x\in\left(x_{k-1},...,x_{k}\right)$
		- $$\varphi\left(x\right)\coloneqq\min_{x_{k-1}\leq\xi\leq x_{k}}f\left(\xi\right)$$
		- $$\psi\left(x\right)\coloneqq\max_{x_{k-1}\leq\xi\leq x_{k}}f\left(\xi\right)$$
	- => $\varphi\left(x\right)\leq f\left(x\right)\leq\psi\left(x\right)$
	- für $x\in\left\lbrack a,b\right\rbrack$ gilt
		- $$\psi\left(x\right)-\varphi\left(x\right)=\max_{x_{k-1}\leq\xi\leq x_{k}}f\left(\xi\right)-\min_{x_{k-1}\leq\xi\leq x_{k}}f\left(\xi\right)$$
-
- ## Satz:
	- reference:: 10.14
	- Jede stetige Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ ist integrierbar
	- Beweis
	  collapsed:: true
		- Satz 10.13 => zu $\varepsilon>0$ gibt es Treppenfunktionen $\varphi\leq f\leq\psi$ mit $\psi-\varphi<\frac{\varepsilon}{2\left(b-a\right)}$
		- => $\int_{a}^{b}\left(\psi-\varphi\right)\leq\int_{a}^{b}\frac{\varepsilon}{2\left(b-a\right)}$
		- also $\left(b-a\right)\cdot\frac{\varepsilon}{2\left(b-a\right)}=\frac{\varepsilon}{2}<\varepsilon$
	- Bemerkung
		- Riemann-Summe:
		  $$\sum_{k=1}^{n}f\left(\xi_{k}\right)\cdot\left(x_{k}-x_{k-1}\right)\approx\int_{a}^{b}f\left(x\right)dx$$
	- Bemerkung
		- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ "stückweise stetig" ist ausreichend
	- Übung
	  collapsed:: true
		- $f:\left\lbrack0,1\right\rbrack\rightarrow\mathbb{R}$ mit $f\left(x\right)=\sin\left(\frac{1}{x}\right)$ für $x\neq0$ und $f\left(0\right)=0$
		- $f\in\mathbb{R}\left\lbrack0,1\right\rbrack$, obwohl bei $x=0$ "sehr unstetig"
		- sei $\varepsilon>0$
		- auf $\left\lbrack\frac{\varepsilon}{5},1\right\rbrack$ ist f stetig, also sogar gleichmäßig stetig
		- => Finde $\varphi\leq f\leq\psi$ auf $\left\lbrack\frac{\varepsilon}{5},1\right\rbrack$ mit $\int_{\frac{\varepsilon}{5}}^1\left(\psi-\varphi\right)<\frac{\varepsilon}{2}$
		- Ergänze $\psi\left(x\right)=1$ und $\varphi\left(x\right)=-1$ auf $\left\lbrack0,\frac{\varepsilon}{5}\right\rbrack$
		- $$\Rightarrow\int_0^1\left(\psi-\varphi\right)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
-