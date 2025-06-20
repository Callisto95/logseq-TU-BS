reference:: 9c

- Satz:
	- reference:: 9.9
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ stetig und in $\left(a,b\right)$ differenzierbar
	- f steigt monoton <=> $\forall x\in\left(a,b\right):f^{\prime}\left(x\right)\geq0$
	  logseq.order-list-type:: number
	- $\left(\forall x\in\left(a,b\right):f^{\prime}\left(x\right)>0\right)\Rightarrow$ f ist streng monoton steigend
	  logseq.order-list-type:: number
	- Beweis
	  collapsed:: true
		- .
		  logseq.order-list-type:: number
			- "=>"
				- sei f monoton steigend
				- $$x\in\left(a,b\right):f^{\prime}\left(x\right)=\lim_{x\rightarrow0}\frac{f\left(x+h\right)-f\left(x\right)}{h}=\lim_{x\downarrow0}\frac{f\left(x+h\right)-f\left(x\right)}{h}\geq0$$
			- "<="
				- sei f nicht monoton steigen
				- => es gibt $s,t\in\left\lbrack a,b\right\rbrack$ mit $s<t$ und $f\left(s\right)>f\left(t\right)$
				- MWS => Es gibt ein $x\in\left(s,t\right)\subseteq\left(a,b\right)$ mit $f^{\prime}\left(x\right)=\frac{f\left(t\right)-f\left(s\right)}{t-s}<0$
		- .
		  logseq.order-list-type:: number
			- sei f nicht streng monoton
			- => $\exists s,t\left\lbrack a,b\right\rbrack:s<t,f\left(s\right)\geq f\left(t\right)$
			- MWS => es gibt ein $x\in\left(s,t\right)$ mit $f^{\prime}\left(x\right)=\frac{f\left(t\right)-f\left(s\right)}{t-s}\leq0$
-
- Satz: **hinreichende Bedingung für Extrema im Inneren**
	- reference:: 9.11
	- $f:\mathbb{R}\rightarrowtail\mathbb{R},x\in\left(\text{Dom}f\right)^{\circ}$ innere Punkt, der sich folgenden Eigenschaften erhält
		- x ist kritisch, d.h. f ist in x differenzierbar mit $f^{\prime}\left(x\right)=0$
		  logseq.order-list-type:: number
		- Es gibt ein $\varepsilon>0$, für das f in $\mathbb{B}_{\varepsilon}\left(x\right)\subseteq\text{Dom}f$ differenzierbar ist
		  logseq.order-list-type:: number
			- außerdem gelte
				- $\forall\xi\in\left(x-\varepsilon,x\right):f^{\prime}\left(\xi\right)\geq0$
				- $\forall\zeta\in\left(x,x+\varepsilon\right):f^{\prime}\left(\zeta\right)\leq0$
			- Dann ist x eine lokale Maximalstelle von f
	- Beweis
		- o.B.d.A. $\left\lbrack x-\varepsilon,x+\varepsilon\right\rbrack\subseteq\text{Dom}f$
		- Satz:9.9 => f steigt in $\left\lbrack x-\varepsilon,x\right\rbrack$ und fällt in $\left\lbrack x,x+\varepsilon\right\rbrack$ monoton
-
- Beispiel: **gehäufte kritische Punkte**
	- reference:: 9.12
	- $f:\mathbb{R}\rightarrow\mathbb{R}$ mit $f\left(x\right)=x^4\cdot\sin^2\frac{1}{x},x\neq0,f\left(0\right)=0$
	- x=0 ist eine Minimalstelle, aber Satz:9.11 funktioniert nicht
-