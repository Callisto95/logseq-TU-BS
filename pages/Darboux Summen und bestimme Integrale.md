reference:: 10b

-
- # Ober- und Unterintegral
	- sei $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ beschränkt
	- Oberintegral
	  $$^{\ast}\int_{a}^{b}\coloneqq\inf\left\lbrace\int_{a}^{b}\psi\middle|\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,f\leq\psi\right\rbrace$$
	- Unterintegral
	  $$_{\ast}\int_{a}^{b}\coloneqq\sup\left\lbrace\int_{a}^{b}\varphi\middle|\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,f\geq\varphi\right\rbrace$$
	- Beispiel
	  collapsed:: true
		- $$f:\left\lbrack0,1\right\rbrack\rightarrow\mathbb{R},f\left(x\right)\coloneqq\left\lbrace_{0,x\notin\mathbb{Q}}^{1,x\in\mathbb{Q}}\right.$$
		- -> effektiv "zwei" Linien, aber keine zwei Punkte auf dem selben $x$
		- $$^{\ast}\int_0^1f=1\neq0=_{\ast}\int_0^1f$$
-
- [[Riemann Integrierbarkeit]]
-
- [[gleichmäßige Stetigkeit]]
-
- # Approximation stetiger Funktionen durch Treppenfunktionen
	- reference:: 10.13
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
- [[Linearität des Integrals]]
- [[Monotonie des Integrals]]
-
- offene Fragen
  collapsed:: true
	- $$\left|f\right|\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- $$f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
-
- # Positiv- und Negativteil einer Funktion
	- reference:: 10.18
	- für $f:\left\lbrack a.b\right\rbrack\rightarrow\mathbb{R}$ heißen $f_{+}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},f_{-}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ mit
	  $$f_{+}\coloneqq\left\lbrace_{0,f\left(x\right)<0}^{f\left(x\right),f\left(x\right)\geq0}\right.,f_{-}\coloneqq\left\lbrace_{-f\left(x\right),f\left(x\right)<0}^{0,f\left(x\right)\geq0}\right.$$
	  der Positiv- bzw. Negativteil von $f$
	- für $x\in\left\lbrack a,b\right\rbrack:$
	  $$f\left(x\right)=f_{+}\left(x\right)-f_{-}\left(x\right),\left|f\left(x\right)\right|=f_{+}\left(x\right)+f_{-}\left(x\right)$$
- ## Satz
	- reference:: 10.19
	- $$f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Rightarrow f_{+}\in\mathbb{R}\left\lbrack a,b\right\rbrack,f_{-}\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- Beweis
	  collapsed:: true
		- sei $\varepsilon>0,\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\leq\psi,\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$
		- $$\Rightarrow\varphi_{+}\leq f_{+}\leq\psi_{+},\psi_{-}\leq f_{-}\leq\varphi_{-}$$
		- Rechne
			- $$\int_{a}^{b}\left(\psi_{+}-\varphi_{+}\right)\leq\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$$
			- $$\int_{a}^{b}\left(\varphi_{-}-\psi_{-}\right)\leq\int_{a}^{b}\left(-\varphi+\psi\right)<\varepsilon$$
-
- Erinnerung
	- $$\left|a+b\right|\leq\left|a\right|+\left|b\right|,\left|\sum_{k=1}^{n}a_{k}\right|\leq\sum_{k=1}^{n}\left|a_{k}\right|$$
-
- # Dreiecksungleichung für Integrale
	- reference:: 10.20
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack$ ist $\left|f\right|\in\mathbb{R}\left\lbrack a,b\right\rbrack$ und
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|\leq\int_{a}^{b}\left|f\left(x\right)\right|dx$$
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|=\pm\int_{a}^{b}f\left(x\right)dx=\int_{a}^{b}\left(\pm f\left(x\right)\right)dx\leq\int_{a}^{b}\left|f\left(x\right)\right|dx$$
-
- [[Integrierbarkeitsregeln]]
-
- Übung:
  collapsed:: true
	- reference:: 10.22
	- $$f,g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- zZ: $f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$
	- Beweis
	  collapsed:: true
		- $$\left(f\left(x\right)\pm g\left(x\right)\right)^2=f\left(x\right)^2\pm2f\left(x\right)g\left(x\right)+g\left(x\right)$$
		- $$\Rightarrow f\left(x\right)\cdot g\left(x\right)=\frac14\left(f\left(x\right)+g\left(x\right)\right)^2-\left(f\left(x\right)-g\left(x\right)\right)^2$$
	- Warnung:
		- $$\int_{a}^{b}f\left(x\right)\cdot g\left(x\right)dx\neq\int_{a}^{b}f\left(x\right)dx\cdot\int_{a}^{b}g\left(x\right)dx$$
-
- Theorem: [[Mittelwertsatz der Integralrechnung]]
-
- Korollar:
	- reference:: 10.24
	- Spezialfall: $w\left(x\right)=1:\forall x\in\left\lbrack a,b\right\rbrack$
	- zu jeder stetigen Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ gibt es ein $\xi\in\left\lbrack a,b\right\rbrack$ mit
	- $$\int_{a}^{b}f\left(x\right)dx=f\left(\xi\right)\cdot\left(b-a\right)$$
-
- # Gewichtsfunktion
	- reference:: 10.25
	- $w:\left\lbrack a,b\right\rbrack\rightarrow\left\lbrack0,\infty\right)$ integrierbar mit $\int_{a}^{b}w\left(x\right)dx\neq0$
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ integrierbar
	- $$M_{w}\left(f\right)\coloneqq\frac{1}{\int_{a}^{b}w\left(x\right)dx}\int_{a}^{b}f\left(x\right)w\left(x\right)dx$$
		- heißt das (mit w) gewichtete Mittel von f über [a,b]
	- $$M\left(f\right)\coloneqq\frac{1}{b-a}\int_{a}^{b}f\left(x\right)dx$$
		- heißt der Mittelwert von f über [a,b]
-