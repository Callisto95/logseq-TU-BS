reference:: 8b

-
- Beispiel
	- $f\left(x\right)=\sin\left(e^{\cos x}\cdot\tanh\left(x^2+z\right)-12x^2\ln x\right)$
	- $\frac{d}{dx}f\left(x\right)=?$
-
- Satz: **linearität des Ableitens**
	- reference:: 8.9
	- seien $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$ in $x\in\left(\text{Dom}f\right)^{\circ}\cap\left(\text{Dom}g\right)^{\circ}$ differenzierbar
	- dann ist für $a,b\in\mathbb{R}$ die Funktion $af\left(x\right)+bg\left(x\right):\mathbb{R}\rightarrowtail\mathbb{R}$ in x differentierbar mit
	- $$\frac{d}{dx}\left(af\left(x\right)+bg\left(x\right)\right)=af^{\prime}\left(x\right)+bg^{\prime}\left(x\right)$$
	- Beweis: Skript
-
- Satz: **Produktregel**
	- reference:: 8.10
	- $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$ seien in $x\in\left(\text{Dom}f\right)^{\circ}\cap\left(\text{Dom}g\right)^{\circ}$ differentierbar
	- => Dann ist die Funktion $f\cdot g:\mathbb{R}\rightarrowtail\mathbb{R},x\mapsto f\left(x\right)\cdot g\left(x\right)$ in x differentierbar
		- dabei $\left(f\cdot g\right)^{\prime}\left(x\right)=f^{\prime}\left(x\right)\cdot g\left(x\right)+f\left(x\right)\cdot g^{\prime}\left(x\right)$
		- $\frac{d}{dx}f\left(x\right)g\left(x\right)=\frac{df\left(x\right)}{dx}\cdot g\left(x\right)+f\left(x\right)\cdot\frac{d\cdot g\left(x\right)}{dx}$
	- Beweis: Skript
-
- Satz: **Kettenregel**
	- reference:: 8.11
	- seien $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$
	- wenn g in $x\in\left(\text{Dom}g\right)^{\circ}$ und f in $y\in\left(\text{Dom}f\right)^{\circ}$ differentierbar sind, dann ist die Verkettung $f\circ g:\mathbb{R}\rightarrowtail\mathbb{R},x\mapsto f\left(g\left(x\right)\right)$ mit $\text{Dom}\left(f\circ g\right)=\left\lbrace x\in\text{Dom}g;g\left(x\right)\in\text{Dom}f\right\rbrace$ im Punkt x differentierbar mit $\frac{d}{dx}f\left(g\left(x\right)\right)=f^{\prime}\left(g\left(x\right)\right)\cdot g^{\prime}\left(x\right)$
	  collapsed:: true
		- aber: Syntax: $\left(f\circ g\right)^{\prime}\left(x\right)$ *NICHT* $\left(f\left(g\left(x\right)\right)\right)^{\prime}$
		- entspannte Schreibweise: $\frac{df}{dx}=\frac{df}{dy}\cdot\frac{dy}{dx}$ mit $y=g\left(x\right)$
	- Beweis
	  collapsed:: true
		- Weil f in y=g(x) differentierbar ist, wird der Differenzenquotient
		- $$\Phi:\text{Dom}f\backslash\left\lbrace y\right\rbrace\rightarrow R,\Phi\left(\eta\right)\coloneqq\frac{f\left(\eta\right)-f\left(y\right)}{\eta-y}$$
		- durch $\Phi\left(y\right)\coloneqq f^{\prime}\left(y\right)$ zu einer in $\eta=y$ stetigen Funktion ergänzt
		- Für $\eta\in\text{Dom}f$ gilt: $f\left(\eta\right)-f\left(y\right)=\Phi\left(\eta\right)\cdot\left(\eta-y\right)$
		- Damit rechne:
		- $$\frac{d}{dx}f\left(g\left(x\right)\right)=\lim_{\xi\rightarrow x}\frac{f\left(g\left(\xi\right)\right)-f\left(g\left(x\right)\right)}{\xi-x}=\lim_{\xi\rightarrow x}\left(\Phi\left(g\left(\xi\right)\right)\cdot\frac{g\left(\xi\right)-g\left(x\right)}{\xi-x}\right)$$
		- Konvergenzen
			- $\Phi\left(g\left(\xi\right)\right)\longrightarrow{}_{}\Phi\left(y\right)=f^{\prime}\left(g\left(x\right)\right)$
			- $\frac{g\left(\xi\right)-g\left(x\right)}{\xi-x}\longrightarrow{}_{}g^{\prime}\left(x\right)$
-
- Übung
  collapsed:: true
	- reference:: 8.12
	- für $a\in\left(0,\infty\right)$ sei die Exponentialgleichungen zur Basis a definiert durch $a^{x}\coloneqq e^{x\cdot\ln a}$
	- Idee: $a^{x}=e^{\ln\left(a^{x}\right)}=e^{x\cdot\ln a}$
	- $$\Rightarrow\frac{d}{dx}a^{x}=\frac{d}{dx}e^{x\cdot\ln a}=\left\lbrack\text{Kettenregel}\right\rbrack=e^{x\cdot\ln a}\cdot\frac{d}{dx}\left(x\cdot\ln a\right)$$
	- dabei
		- $g\left(x\right)\coloneqq x\cdot\ln a$
		- äußere Ableitung: $e^{x\cdot\ln a}$
		- innere Ableitung: $\frac{d}{dx}\left(x\cdot\ln a\right)$
	- $$=a^{x}\cdot\ln a$$
-
- Übung
  collapsed:: true
	- reference:: 8.13
	- $f:\mathbb{R}\rightarrow\mathbb{R}$ mit $f\left(x\right)\coloneqq\sin\left(x^2\cdot2^{x}\right)$
	- $$\frac{d}{dx}f\left(x\right)=\frac{d}{dx}\sin\left(x^2\cdot2^{x}\right)=^{\text{KR}}\cos\left(x^2\cdot2^{x}\right)\cdot\frac{d}{dx}\left(x^2\cdot2^{x}\right)=\cos\left(x^2\cdot2^{x}\right)\cdot\left(\frac{d}{dx}2^{x}+x^2\cdot\frac{d2^{x}}{dx}\right)$$
	- $$=\cos\left(x^2\cdot2^{x}\right)\left(2x\cdot2^{x}+x^2\cdot2^{x}\cdot\ln2\right)$$
-
- Korollar: **Quotientenregel**
	- reference:: 8.14
	- $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$ seien in $x\in\left(\text{Dom}f\right)^{\circ}\cap\left(\text{Dom}g\right)^{\circ}$ differentierbar
	- Außerdem gelte $g\left(x\right)\neq0$
	- $$\Rightarrow\frac{f}{g}:\mathbb{R}\rightarrowtail\mathbb{R},x\mapsto\frac{f\left(x\right)}{g\left(x\right)}$$
	- ist in x differentierbar mit
	- $$\frac{d}{dx}\frac{f\left(x\right)}{g\left(x\right)}=\frac{f^{\prime}\left(x\right)g\left(x\right)-f\left(x\right)g^{\prime}\left(x\right)}{\left(g\left(x\right)\right)^2}$$
	- Beweis
	  collapsed:: true
		- Hausaufgabe
		- $$\frac{f\left(x\right)}{g\left(x\right)}=f\left(x\right)\cdot\frac{1}{g\left(x\right)}$$
-
- Satz: **Ableiten von Umkehrfunktionen**
	- reference:: 8.15
	- sei $I=\left(a,b\right)\subseteq\mathbb{R}$ ein offenes [[Intervall]], sei $f:I\rightarrow\mathbb{R}$ stetig und streng monoton
	- Wenn f in $x\in\left(a,b\right)$ differentierbar ist mit $f^{\prime}\left(x\right)\neq0$
	- => $f^{-1}$ ist in $y\coloneqq f\left(x\right)$ differentierbar, und es gilt
	- $$\left(f^{-1}\right)^{\prime}\left(y\right)=\frac{d}{dy}f^{-1}\left(y\right)=\frac{1}{f^{\prime}\left(x\right)}=\frac{1}{f^{\prime}\left(f^{-1}\left(y\right)\right)}$$
	- Beweis
	  collapsed:: true
		- zZ: $\lim_{v\rightarrow y}\frac{f^{-1}\left(v\right)-f^{-1}\cdot y}{x-y}=\frac{1}{f^{\prime}\left(x\right)}$ mit $x=f^{\prime}\left(y\right)$
		- sei dazu $\left(v_{k}\right)_{k=1}^{\infty}\subseteq\text{Ran}f\backslash\left\lbrace y\right\rbrace$ eine beliebige Folge mit $v_{k}\longrightarrow{}_{k\rightarrow\infty}y$
		- => $f^{-1}$ ist stetig
		- => Durch $u_{k}\coloneqq f^{-1}\left(u_{k}\right)$ wird eine Folge $\left(u_{k}\right)_{k=1}^{\infty}\subseteq I\backslash\left\lbrace x\right\rbrace$ definiert mit
		- $$\lim_{k\rightarrow\infty}u_{k}=\lim_{k\rightarrow\infty}f^{-1}\left(v_{k}\right)=f^{-1}\left(\lim_{k\rightarrow\infty}v_{k}\right)=f^{-1}\left(y\right)=x$$
		- $$\Rightarrow\frac{f^{-1}\left(v_{k}\right)-f^{-1}\left(y\right)}{v_{k}-y}=\frac{u_{k}-x}{f\left(u_{k}\right)-f\left(x\right)}=\frac{1}{\frac{f\left(u_{k}\right)-f\left(x\right)}{u_{k}-x}}\longrightarrow{}_{k\rightarrow\infty}\frac{1}{f^{\prime}\left(x\right)}$$
	- Notiz
	  collapsed:: true
		- $f^{-1}\left(f\left(x\right)\right)=x\Rightarrow\frac{d}{dx}f^{-1}\left(f\left(x\right)\right)=1\Rightarrow\frac{df^{-1}}{dy}\left(f\left(x\right)\right)\cdot f^{\prime}\left(x\right)=1$
-
- Übung
  collapsed:: true
	- reference:: 8.16
	- $$\frac{d}{dy}\ln y=\frac{1}{\left(\frac{d}{dx}e^{x}\right)_{x=\ln y}}=\left(\frac{1}{e^{x}}\right)_{x=\ln y}=\frac{1}{e^{\ln y}}=\frac{1}{y}$$
-