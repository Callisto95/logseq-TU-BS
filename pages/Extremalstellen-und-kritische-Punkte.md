reference:: 9a

-
- Satz: **notwendige Bedingung für Extrema**
	- reference:: 9.1
	- $f:\mathbb{R}\rightarrowtail\mathbb{R},x\in\left(\text{Dom}f\right)^{\circ}$ sei eine Extremalstelle
	- Außerdem sei f in x differentierbar
	- => $f^{\prime}\left(x\right)=0$
	- Beweis
	  collapsed:: true
		- sei o.B.d.A. x eine lokale Maximalstelle
		- Es gibt ein $\varepsilon>0$ mit $\mathbb{B}_{\varepsilon}\left(x\right)=\left(x-\varepsilon,x+\varepsilon\right)\subseteq\text{Dom}f$ und $\forall\xi\in\mathbb{B}_{\varepsilon}\left(x\right):f\left(\xi\right)\leq f\left(x\right)$
		- Dann gilt
			- $$f^{\prime}\left(x\right)=\lim_{\xi\rightarrow x}\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}=\lim_{\xi\downarrow x}\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}\leq0$$
			- $$f^{\prime}\left(x\right)=\lim_{\xi\rightarrow x}\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}=\lim_{\xi\uparrow x}\frac{f\left(\xi\right)-f\left(x\right)}{\xi-x}\geq0$$
			- $$\Rightarrow f^{\prime}\left(x\right)=0$$
	- Beispiel
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq x^3,f^{\prime}\left(x\right)=3x^2,f^{\prime}\left(0\right)=0$
		- aber x=0 ist hier keine Extremalstelle
		- -> Bedingung ist nur notwendig
-
- Defintion: **kritische Punkte**
	- reference:: 9.2
	- für $f:\mathbb{R}\rightarrowtail\mathbb{R}$ heißen $x\in\left(\text{Dom}f\right)^{\circ}$, in deren f differentierbar ist mit $f^{\prime}\left(x\right)=0$ kritische Punkte von f
-
- Übung
  collapsed:: true
	- reference:: 9.3
	- $f:\mathbb{R}\rightarrowtail\mathbb{R}$ mit $f\left(x\right)\coloneqq\left(1+4x\right)e^{-2x}$
	- Gesucht: Kritische Punkte
	- Ableitung:
	- $$\frac{d}{dx}f\left(x\right)=\frac{d}{dx}\left(\left(1+4x\right)e^{-2x}\right)=^{\text{PR}}\frac{d\left(1+4x\right)}{dx}\cdot e^{-2x}+\left(1+4x\right)\frac{de^{-2x}}{dx}$$
	- $$=^{\text{KR}}4e^{-2x}+\left(1+4x\right)e^{-2x}\frac{d}{dx}\left(-2x\right)=4e^{-2x}+\left(1+4x\right)e^{-2x}\cdot\left(-2\right)$$
	- $$=e^{-2x}\left(2-8x\right)=0?$$
	- $$f^{\prime}\left(x\right)=0\Leftrightarrow x=\frac14$$
	- $\frac14$ als einzelner kritischer Punkt
-