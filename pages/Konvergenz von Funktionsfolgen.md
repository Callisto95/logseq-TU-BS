reference:: 6d

- $$e^{x}=\lim_{n\rightarrow\infty}\sum_{k=0}^{n}\frac{x^{k}}{k!}=\lim_{n\rightarrow\infty}\left(1+\frac{x}{1!}+\frac{x^2}{2!}+...+\frac{x^{n}}{n!}\right)$$
- mit
	- $f_0\left(x\right)=1$
	- $f_1\left(x\right)=x$
	- $f_2\left(x\right)=x^2$, aber verschoben nach unten links
	- => alle gehen durch Punkt $\left(0,1\right)$
- $$\exp x=\sum_{k=0}^{\infty}\frac{x^{k}}{k!}=\lim_{n\rightarrow\infty}\sum_{k=0}^{n}\frac{x^{k}}{k!}$$
	- $$f_{n}\left(x\right)\coloneqq\sum_{k=0}^{n}\frac{x^{k}}{k!}$$
	- stetige Polynomfunktion
-
- Beispiel
	- $$g_{n}\left(x\right)\coloneqq\frac{nx}{1+\left|nx\right|}$$
	- $$\lim_{n\rightarrow\infty}g_{n}\left(x\right)=\lim_{n\rightarrow\infty}\frac{x}{\frac{1}{n}+\left|x\right|}=\left\lbrack x\neq0\right\rbrack=\frac{x}{\left|x\right|}=\left\lbrace_{-1,x<0}^{1,x>0}\right.0,x=0$$
	- => Grenzfunktion ist unstetig
-
- Problem: "Konvergenzgeschwindigkeit" hängt von $x$ ab
-
- # gleichmäßige und punktmäßige Konvergenz
	- reference:: 6.15
	- $D\subseteq\mathbb{R},\left(f_{n}\right)_{n=1}^{\infty}$ mit $f_{n}:D\rightarrow\mathbb{R}$ "Funktionsfolge"
- ## punktweise Konvergenz
	- $\left(f_{n}\right)_{n=0}^{\infty}$ konvergiert Punktweise gegen eine Grenzfunktion $f:D\rightarrow\mathbb{R}$, (genau dann) wenn
	  $$\forall x\in D:f_{n}\left(x\right)\longrightarrow{}_{n\rightarrow\infty}f\left(x\right)$$
	- d.h.
	  $$\forall x\in D:\forall\varepsilon>0:\exists m\in\mathbb{N}:\forall n\geq m:\left|f_{n}\left(x\right)-f\left(x\right)\right|<\varepsilon$$
		- mit $m=m\left(\varepsilon,x\right)$
- ## gleichmäßige Konvergenz
	- $\left(f_{n}\right)_{n=1}^{\infty}$ konvergiert gleichmäßig gegen $f:D\rightarrow\mathbb{R}$, wenn
	- $$\forall\varepsilon>0:\exists m\in\mathbb{N}:\forall n\geq m:\forall x\in D:\left|f_{n}\left(x\right)-f\left(x\right)\right|<\varepsilon$$
		- mit $m=m\left(\varepsilon\right)\neq m\left(\varepsilon,x\right)$
		- Unterschied zu Punktkonvergenz: gilt für alle Punkte, nicht nur einem
		- auch:
		  $$\forall\varepsilon:\exists m\in\mathbb{N}:\forall n\geq m:\sup_{x\in D}\left|f_{n}\left(x\right)-f\left(x\right)\right|\leq\varepsilon$$
			- dabei
			  $$\sup_{x\in D}\left|f_{n}\left(x\right)-f\left(x\right)\right|=\left|\left|f_{n}-f\right|\right|_{\infty}$$
			  Als "Supremumsnorm"
-
- Problem: Stetigkeit Überlebt im Allgemeinen punktweise Konvergenz nicht
	- $1_{\left\lbrack0,1\right\rbrack}\left(x\right)\coloneqq\left\lbrace_{0,\text{ sonst}}^{1,x\in\left\lbrack0,1\right\rbrack}\right.$
-
- 7.2.2
	- $$D\subseteq\mathbb{R},\left(f_{n}\right)_{n=1}^{\infty}\subseteq C\left(D\right)$$
		- also $f_{n}:D\rightarrow\mathbb{R}$ stetig
	- sei $f:D\rightarrow\mathbb{R}$
	- Wenn $\left(f_{n}\right)_{n=1}^{\infty}$ gleichmäßig gegen $f$ konvergiert, dann ist $f$ stetig
	- Beweis
	  collapsed:: true
		- seien $\varepsilon>0,\xi\in D$
		- dann gibt es ein $n\in\mathbb{N}$ mit
		  $$\sup_{x\in D}\left|f_{n}\left(x\right)-f\left(x\right)\right|<\frac{\varepsilon}{3}$$
			- gilt theoretisch für alle $n$ ab einem Schwellenwert; nur eine ist benötigt
		- $f_{n}$ stetig => es gibt ein $\delta>0$ mit
		  $$\forall x\in D:\left|x-\xi\right|<\delta\Rightarrow\left|f_{n}\left(x\right)-f_{n}\left(\xi\right)\right|<\frac{\varepsilon}{3}$$
		- $$\forall x\in D:\left|x-\xi\right|<\delta:$$
		  $$\left|f\left(x\right)-f\left(\xi\right)\right|=\left|f\left(x\right)-f_{n}\left(x\right)+f_{n}\left(x\right)-f_{n}\left(\xi\right)+f_{n}\left(\xi\right)-f\left(\xi\right)\right|$$
		  $$\leq\left|f\left(x\right)-f_{n}\left(x\right)\right|+\left|f_{n}\left(x\right)-f_{n}\left(\xi\right)\right|+\left|f_{n}\left(\xi\right)-f\left(\xi\right)\right|$$
		  $$<\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon$$
-
- Frage: Konvergieren Potenzreiehen (im Allgemeinen) gleichmäßig?
	- => Nein.
	- Beweis
	  collapsed:: true
		- für $x\in\left(-1,1\right)$ gilt:
		  $$\sum_{k=0}^{\infty}x^{k}=\frac{1}{1-x}\eqqcolon f\left(x\right)$$
		- $$f_{n}\left(x\right)\coloneqq\sum_{k=0}^{n}x^{k},D=\left(-1,1\right)$$
		- Potenzreihe $\sum_{k=0}^{\infty}x^{k}$ hat Konvergenzradius $r=1$ zur gleichmäßigen Konvergenz
		- $$\sup_{x\in D}\left|\sum_{k=1}^{n}x^{k}-\frac{1}{1-x}\right|=\sup_{x\in D}\left|\frac{1-x^{n+1}}{1-x}-\frac{1}{1-x}\right|=\sup_{x\in D}\frac{\left|x\right|^{n+1}}{1-x}=\infty$$
	- Lösung: Schaue die Potenzreihe in einem Kleineren Definitionsbereich an
- ## lokal gleichmäßige Konvergenz
	- $$\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}$$
	  sei eine (reelle) [[Potenzreihe]] mit Konvergenzradius $r\in\left(0,\infty\right\rbrack$
	- Außerdem sei $s\in\left(0,r\right)$
	- Dann konvergiert sie Potenzreihe in der abgeschlossenen Umgebung $\overline{B_{s}\left(x_0\right)}=\left\lbrack x_0-s,x_0+s\right\rbrack$ gleichmäßig
	- Beweis
		- sei $\varepsilon>0$
		- für $n\in\mathbb{N}$ gilt zunächst:
		  $$\left|\sum_{k=0}^{\infty}a_{k}\left(x-x_0\right)^{k}-\sum_{k=0}^{n}a_{k}\left(x-x_0\right)^{k}\right|=\left|\sum_{k=n+1}^{\infty}a_{k}\left(x-x_0\right)^{k}\right|\leq\sum_{k=n+1}^{\infty}\left|a_{k}\right|\cdot\left\lbrack\left|x-x_0\right|\right\rbrack_{\leq s}^{k}\leq\sum_{k=n+1}^{\infty}\left|a_{k}\right|\cdot s^{k}$$
		- => $\sum_{k=0}^{\infty}a_{k}s^{k}$ konvergiert absolut
		- => nach [[cauchy]] gibt es ein $n\in\mathbb{N}$:
		  $$\sum_{k=n+1}^{\infty}\left|a_{k}\right|\cdot s^{k}<\varepsilon$$
-