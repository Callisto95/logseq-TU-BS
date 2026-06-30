reference:: 10b

-
- [[Integrierbarkeitsregeln]]
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
- [[gleichmäßige Stetigkeit]]
- [[Approximation stetiger Funktionen durch Treppenfunktionen]]
- [[Monotonie des Integrals]]
-
- offene Fragen
  collapsed:: true
	- $$\left|f\right|\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- $$f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
-
- [[Positiv- und Negativteil einer Funktion]]
- [[Dreiecksungleichung von Integralen]]
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
- [[Gewichtsfunktion bei Integralen]]
-