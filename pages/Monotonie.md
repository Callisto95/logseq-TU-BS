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
- Übung
	- reference:: 9.10
	- (eigentlich Beweis)
	- $f:\mathbb{R}\rightarrow\mathbb{R}$ mit $f\left(x\right)=x^3$ steigt streng monoton