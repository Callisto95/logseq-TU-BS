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
	- Wenn $\left(f_{n}\right)_{k=1}^{\infty}$