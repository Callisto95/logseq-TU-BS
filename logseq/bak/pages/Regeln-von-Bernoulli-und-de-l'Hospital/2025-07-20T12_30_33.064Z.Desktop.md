reference:: 13a

-
- Ziel: Grenzwerte vom Typ $\frac00,\frac{\pm\infty}{\pm\infty},1^{\infty},0^0$
	- $\left(1+\frac{1}{n}\right)^{n}\longrightarrow{}_{n\rightarrow\infty}e\rightsquigarrow\left(1+\frac{1}{x}\right)^{x}\longrightarrow{}_{x\rightarrow\infty}e$
	- Spezialfall: <Bild>
	- Idee: $\lim_{\xi\rightarrow x}\frac{f\left(\xi\right)}{f\left(\xi\right)}=\lim_{t\rightarrow0}\frac{f\left(x+t\right)}{g\left(x+t\right)}$
		- [[Taylor-Polynom]]:
			- $$f\left(x+t\right)=f\left(x\right)+tf^{\prime}\left(x\right)+t\rho\left(t\right)$$
				- mit $\rho\left(t\right)\longrightarrow{}_{t\rightarrow0}0$
			- $$g\left(x+t\right)=g\left(x\right)+tg^{\prime}\left(x\right)+t\sigma\left(t\right)$$
				- mit $\sigma\left(t\right)\longrightarrow{}_{t\rightarrow0}0$
		- $$\frac{f\left(x+t\right)}{g\left(x+t\right)}=\frac{f\left(x\right)+tf^{\prime}\left(x\right)+t\rho\left(t\right)}{g\left(x\right)+tg^{\prime}\left(x\right)+t\sigma\left(t\right)}$$
			- da $f\left(x\right)=0,g\left(x\right)=0$ (Spezialfall)
		- $$=\frac{f^{\prime}\left(x\right)+\rho\left(t\right)}{g^{\prime}\left(x\right)+\sigma\left(t\right)}\longrightarrow{}_{t\rightarrow0}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
		- Beispiel
			- $$\lim_{x\rightarrow0}\frac{\sin x}{x}=\lim_{x\rightarrow0}\frac{\frac{d}{dx}\sin x}{\frac{d}{dx}x}=\lim_{x\rightarrow0}\frac{\cos x}{1}=\frac11=1$$
-
- Satz: **Regel von Bernoulli und de l'Hospital**
	- reference:: 13.1
	- sei $\left(a,b\right)\subseteq\mathbb{R};a,b\in\mathbb{R};f:\left(a,b\right)\rightarrow\mathbb{R};g\left(a,b\right)\rightarrow\mathbb{R}$ differentierbar
	- Es gelte $g\left(x\right)\neq0\neq g^{\prime}\left(x\right)$ und $\lim_{x\uparrow b}f\left(x\right)=0=\lim_{x\uparrow b}g\left(x\right)$
	- Wenn der (eigentlich ungleiche) Grenzwert
	- $$\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}\in\mathbb{R}\cup\left\lbrace\infty,-\infty\right\rbrace$$
	- exisitert, dann konvergiert (bzw. divergiert bestimmt)
	- $$\lim_{x\uparrow b}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
	- Beweis
	  collapsed:: true
		- Ergänze f,g stetig durch $f\left(b\right)\coloneqq0,g\left(b\right)\coloneqq0$
		- $$\frac{f\left(x\right)}{g\left(x\right)}=\frac{0-f\left(x\right)}{0-g\left(x\right)}=\frac{f\left(b\right)-f\left(x\right)}{g\left(b\right)-g\left(x\right)}=^{\text{zZ}}\frac{f\left(b\right)-f\left(x\right)}{b-x}\cdot\frac{b-x}{g\left(b\right)-g\left(x\right)}$$
		- Problem beim MWS
			- $$\frac{f\left(b\right)-f\left(x\right)}{b-x}=f^{\prime}\left(\xi_{x}\right);\frac{g\left(b\right)-g\left(x\right)}{b-x}=g^{\prime}\left(\xi_{x}\right)$$
			- im Allgemeinen $\xi_{x}\neq\xi_{x}$?
		- zZ: 13.2:
			- $$\exists\xi_{x}\in\left(x,b\right):g^{\prime}\left(\xi_{x}\right)\cdot\left(f\left(b\right)-f\left(x\right)\right)=f^{\prime}\left(\xi_{x}\right)\cdot\left(g\left(b\right)-g\left(x\right)\right)$$
			- $$\Rightarrow\frac{f\left(x\right)}{g\left(x\right)}=\frac{f^{\prime}\left(\xi_{x}\right)}{g^{\prime}\left(\xi_{x}\right)}\longrightarrow{}_{x\uparrow b}\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
			- Hilfsfunktion
				- $$h:\left\lbrack x,b\right\rbrack\rightarrow\mathbb{R},h\left(t\right)\coloneqq\left(g\left(t\right)-g\left(x\right)\right)\cdot\left(f\left(b\right)-f\left(x\right)\right)-\left(f\left(t\right)-f\left(x\right)\right)\cdot\left(g\left(b\right)-g\left(x\right)\right)$$
				- $$h\left(x\right)=0\cdot\left(f\left(b\right)-f\left(x\right)\right)-0\cdot\left(g\left(b\right)-g\left(x\right)\right)=0$$
				- $$h\left(b\right)=\left(g\left(b\right)-g\left(x\right)\right)\cdot\left(f\left(b\right)-f\left(x\right)\right)-\left(f\left(b\right)-f\left(x\right)\right)\cdot\left(g\left(b\right)-g\left(x\right)\right)=0$$
			- Rolle (Lemma 9.4):
				- $$\Rightarrow\exists\xi_{x}\in\left(x,s\right):h^{\prime}\left(\xi_{x}\right)=0$$
				- $$h^{\prime}\left(t\right)=g^{\prime}\left(t\right)\cdot\left(f\left(b\right)-f\left(x\right)\right)-f^{\prime}\left(t\right)\cdot\left(g\left(b\right)-g\left(x\right)\right)$$
				- $$\Rightarrow0=h^{\prime}\left(\xi_{x}\right)=g^{\prime}\left(\xi_{x}\right)\left(f\left(b\right)-f\left(x\right)\right)-f^{\prime}\left(\xi_{x}\right)\left(g\left(b\right)-g\left(x\right)\right)$$
	- Ziel
	  collapsed:: true
		- $$\left(1+\frac{1}{n}\right)^{n}\longrightarrow{}_{n\rightarrow\infty}e$$
		- $$\left(1+\frac{1}{x}\right)^{x}\longrightarrow{}_{x\rightarrow\infty}e$$
	- Bemerkung: statt $I=\left(a,b\right)$ gilt auch $I=\left(a,\infty\right)$:
		- $$\lim_{x\rightarrow\infty}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{y\downarrow0}\frac{f\left(\frac{1}{y}\right)}{g\left(\frac{1}{y}\right)}=^{\text{l'Hop}}\lim_{y\downarrow0}\frac{\frac{d}{dy}f\left(\frac{1}{y}\right)}{\frac{d}{dy}g\left(\frac{1}{y}\right)}$$
		- $$=\lim_{y\downarrow0}\frac{f^{\prime}\left(\frac{1}{y}\right)\frac{d}{dy}\frac{1}{y}}{g^{\prime}\left(\frac{1}{y}\right)\frac{d}{dy}\frac{1}{y}}=\lim_{x\rightarrow\infty}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
	- Beispiel: Typ $1^{\infty}$
	  collapsed:: true
		- $$\lim_{x\rightarrow\infty}\left\lbrack\left(1+\frac{1}{x}\right)^{x}\right\rbrack_1\left\lbrack=\right\rbrack_2\lim_{x\rightarrow\infty}\exp\left(x\cdot\ln\left(1+\frac{1}{x}\right)\right)$$
			- $\left(1+\frac{1}{x}\right)^{x}$ vom Typ $1^{\infty}$
			  logseq.order-list-type:: number
			- logseq.order-list-type:: number
			  $$a^{b}\equiv e^{\ln a^{b}}=e^{b\cdot\ln a}$$
		- $$\lim_{x\rightarrow\infty}x\cdot\ln\left(1+\frac{1}{x}\right)=\lim_{x\rightarrow\infty}\frac{\ln\left(1+\frac{1}{x}\right)}{\frac{1}{x}}$$
		- $$=_{\text{???}}^{\text{l'Hop}}\lim_{x\rightarrow\infty}\frac{\frac{d}{dx}\ln\left(1+\frac{1}{x}\right)}{\frac{d}{dx}\frac{1}{x}}=\lim_{x\rightarrow\infty}\frac{\frac{1}{1+\frac{1}{x}}\cdot\frac{d}{dx}\left(1+\frac{1}{x}\right)}{\frac{d}{dx}\frac{1}{x}}=1$$
		- $$\Rightarrow\lim_{x\rightarrow\infty}\left(1+\frac{1}{x}\right)^{x}=\exp\left(\lim_{x\rightarrow\infty}\frac{\ln\left(1+\frac{1}{x}\right)}{\frac{1}{x}}\right)=\exp1=e$$
		- $$\rightarrow\lim_{x\rightarrow\infty}\left(1+\frac{1}{n}\right)^{n}=e=\sum_{k=0}^{\infty}\frac{1}{k!}$$
	- Beispiel: Typ $\frac{\infty}{\infty}$
		- NEIN:
			- $$\frac{f\left(x\right)}{g\left(x\right)}=\frac{\frac{1}{g\left(x\right)}}{\frac{1}{f\left(x\right)}}=_{\text{??? lim}}^{\text{l'Hop}}\frac{\frac{d}{dx}\frac{1}{g\left(x\right)}}{\frac{d}{dx}\frac{1}{f\left(x\right)}}=\frac{-\frac{g^{\prime}\left(x\right)}{g\left(x\right)^2}}{-\frac{f^{\prime}\left(x\right)}{f\left(x\right)^2}}=\frac{g^{\prime}\left(x\right)}{f^{\prime}\left(x\right)}\cdot\frac{f\left(x\right)^2}{g\left(x\right)^2}$$
		- Idee: Spezialfall $g\left(x\right)=x,x\rightarrow\infty$
-
- Lemma:
	- reference:: 13.2
	- sei $h:\left(c,\infty\right)\rightarrow\mathbb{R}$ differentierbar mit $\lim_{t\rightarrow\infty}h^{\prime}\left(t\right)=\lambda$
	- Dann gilt $\frac{h\left(t\right)}{t}\longrightarrow{}_{t\rightarrow\infty}\lambda$
	- Beweis
		- $$\frac{h\left(t\right)-\lambda t}{t}\longrightarrow{}_{t\rightarrow\infty}^{\text{???}}0$$
			- $$\frac{h\left(t\right)-\lambda t}{t}=\frac{h\left(t\right)}{t}-\lambda\longrightarrow{}_{t\rightarrow\infty}^{\text{zZ}}0$$
		- $$\frac{d}{dt}\left(h\left(t\right)-\lambda t\right)=h^{\prime}\left(t\right)-\lambda\longrightarrow{}_{t\rightarrow\infty}0$$
			- sei $u\coloneqq h\left(t\right)-\lambda t$
		- sei $\varepsilon>0$
			- => $\exists T>\max\left\lbrace c,0\right\rbrace$ mit
			- $$\forall t\in\left\lbrack T,\infty\right):\left|u^{\prime}\left(t\right)\right|\leq\frac{\varepsilon}{2}$$
			- $$\Rightarrow\forall t\in\left\lbrack T,\infty\right):\left|u\left(t\right)-u\left(T\right)\right|\leq\frac{\varepsilon}{2}\left(t-T\right)$$
			- Wenn $t\geq\frac{2\cdot\left|u\left(T\right)\right|}{\varepsilon}$, dann
				- $$\left|\frac{u\left(t\right)}{t}\right|\leq\frac{\left|u\left(T\right)\right|}{t}+\frac{\left|u\left(t\right)-u\left(T\right)\right|}{t}\leq\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
				- $$\Rightarrow\left|\frac{h\left(t\right)}{t}-\lambda\right|\longrightarrow{}_{t\rightarrow\infty}0$$
				- $$\Rightarrow\lim_{t\rightarrow\infty}\frac{h\left(t\right)}{t}=\lim_{t\rightarrow\infty}\frac{h^{\prime}\left(t\right)}{1}=\lambda$$
-
- Satz: **Regel von Bernoulli und de l'Hospital** Typ $\frac{\infty}{\infty}$
	- reference:: 13.3
	- sei $I=\left(a,b\right)\subseteq\mathbb{R};a,b\in\mathbb{R};f,g:I\rightarrow\mathbb{R}$ differentierbar
	- mit $\forall x\in I:g\left(x\right)\neq0\neq g^{\prime}\left(x\right)$
	- außerdem: $\lim_{x\uparrow b}g\left(x\right)=\pm\infty$
	- Wenn
		- $$\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}\in\mathbb{R}\cup\left\lbrace\infty,-\infty\right\rbrace$$
	- existiert, dann
		- $$\lim_{x\uparrow b}\frac{f\left(x\right)}{g\left(x\right)}=\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
	- Idee:
	  collapsed:: true
		- Substituiere $x=g^{-1}\left(t\right),t\coloneqq g\left(x\right)$
		- Bildinervall: $J\coloneqq g\left(I\right)$ mit $\forall x\in I:g^{\prime}\left(x\right)\neq0$
			- Rolle: g injektiv
		- $g:I\rightarrow J$ bijektiv
		- $g^{-1}:J\rightarrow I$
		- Hilfsfunktion:
			- $h:J\rightarrow\mathbb{R},h\left(t\right)\coloneqq f\left(g^{-1}\left(t\right)\right)$
			- dabei: $h\left(g\left(x\right)\right)=f\left(g^{-1}\left(g\left(x\right)\right)\right)=f\left(x\right)$
		- $g\left(x\right)\longrightarrow{}_{x\uparrow b}\pm\infty$ => J ist unbeschränkt
		- Rechne
			- $\frac{d}{dt}h\left(t\right)=\frac{d}{dt}f\left(g^{-1}\left(t\right)\right)\left\lbrack=\right\rbrack_1\frac{f^{\prime}\left(g^{\prime}\left(t\right)\right)}{g^{\prime}\left(g^{-1}\left(t\right)\right)}$
				- Kettenregel, $\frac{d}{dt}g^{-1}\left(t\right)=\frac{1}{g^{\prime}\left(g^{-1}\left(t\right)\right)}$
				  logseq.order-list-type:: number
			- $$...\longrightarrow{}_{t\rightarrow\pm\infty}\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}=\lambda$$
		- Lemma 13.2 mit $t=g\left(x\right)$
			- $$\lim_{x\uparrow b}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}=\lambda=\lim_{t\rightarrow\pm\infty}h^{\prime}\left(t\right)=^{\text{13.2}}\lim_{t\rightarrow\pm\infty}\frac{h\left(t\right)}{t}=\lim_{x\uparrow b}\frac{f\left(x\right)}{g\left(x\right)}$$
-
- Übungen:
	- reference:: 13.4
	- logseq.order-list-type:: number
	  $$\lim_{x\rightarrow1}\frac{\ln x}{x-1}$$
		- $$=^{\text{l'Hop}}\lim_{x\rightarrow1}\frac{\frac{d}{dx}\ln x}{\frac{d}{dx}\left(x-1\right)}=\lim_{x\rightarrow1}\frac{\frac{1}{x}}{1}=\frac{\frac11}{1}=1$$
	- logseq.order-list-type:: number
	  $$\lim_{x\rightarrow\infty}\frac{\ln x}{x}$$
		- $$=^{\text{l'Hop}}\frac{\frac{d}{dx}\ln x}{\frac{d}{dx}x}=\lim_{x\rightarrow\infty}\frac{\frac{1}{x}}{1}=0$$
	- logseq.order-list-type:: number
	  $$\lim_{x\downarrow0}x^{x}$$
		- $$=\lim_{x\downarrow0}\exp\left(x\cdot\ln x\right)=\exp\left(\lim_{x\downarrow0}\frac{\ln x}{\frac{1}{x}}\right)=^{\text{l'Hop}}\exp\left(\lim_{x\downarrow0}\frac{\frac{d}{dx}\ln x}{\frac{d}{dx}\frac{1}{x}}\right)=\exp\left(\lim_{x\downarrow0}\frac{\frac{1}{x}}{-\frac{1}{x^2}}\right)$$
		- $$=\exp\left(\lim_{x\downarrow0}\frac{-x^2}{x}\right)=\exp\left(0\right)=1$$
		- Notiz: $\lim_{a,b\downarrow0}a^{b}=\lim_{a,b\downarrow0}\exp\left(b\cdot\ln a\right)$
	- logseq.order-list-type:: number
	  $$\lim_{x\downarrow0}\left(e^{-\frac{1}{x^2}}\right)^{x}$$
		- $$=\lim_{x\downarrow0}\exp\left(x\cdot\ln\left(e^{-\frac{1}{x^2}}\right)\right)=\lim_{x\downarrow0}\exp\left(-\frac{x}{x^2}\right)=\exp\left(\lim_{x\downarrow0}\left(-\frac{1}{x}\right)\right)=0$$
	- logseq.order-list-type:: number
	  $$\lim_{x\downarrow0}\frac{2\sin x-x^2-2x}{\sinh x^2}$$
		- $$=\lim_{x\downarrow0}\frac{2\cos x-2x-2}{\cosh x^2\cdot2x}=^{\text{l'Hop}}\lim_{x\rightarrow0}\frac{\frac{d}{dx}\left(2\cos x-ex-2\right)}{\frac{d}{dx}\left(\cosh x^2\cdot2x\right)}$$
		- $$=\lim_{x\rightarrow0}\frac{-2\sin x-2}{\sinh x^2\cdot4x^2+\cosh x^2\cdot2}=\frac{0-2}{0+2}=-1$$
-
- Gegenbeispiele:
	- logseq.order-list-type:: number
	  $$\lim_{x\rightarrow1}\frac{3x^2+2x-1}{2x}$$
		- $$=\frac12$$
		- Vergleich
			- l'Hopital erzwungen:
			- $$\lim_{x\rightarrow1}\frac{\frac{d}{dx}\left(3x^2+2x-1\right)}{2x}=\lim_{x\rightarrow1}\frac{6x+2}{2}=\frac{6+2}{2}=4$$
	- logseq.order-list-type:: number
	  $$f\left(x\right)\coloneqq x+\sin x\cdot\cos x$$
		- $$g\left(x\right)\coloneqq f\left(x\right)\cdot e^{\sin x}$$
		- $$\lim_{x\rightarrow\infty}\frac{f\left(x\right)}{g\left(x\right)}=???$$
		- existiert Grenzwert?
			- $$\frac{f\left(x\right)}{g\left(x\right)}=\frac{f\left(x\right)}{f\left(x\right)\cdot e^{\sin x}}=e^{-\sin x}$$
			- $$\Rightarrow\nexists\lim_{x\rightarrow\infty}\frac{f\left(x\right)}{g\left(x\right)}$$
		- Frage: funktioniert l'Hospital?
			- $$f\left(x\right)=x+\sin x\cdot\cos x\longrightarrow{}_{x\rightarrow\infty}\infty$$
			- $$g\left(x\right)=f\left(x\right)\cdot e^{\sin x}\longrightarrow{}_{x\rightarrow\infty}\infty$$
			- $$f^{\prime}\left(x\right)=1+\cos^2x-\sin^2x$$
			- $$g^{\prime}\left(x\right)=\frac{d}{dx}\left(f\left(x\right)\cdot e^{\sin x}\right)=f^{\prime}\left(x\right)\cdot e^{\sin x}+\cos x\cdot f\left(x\right)+e^{\sin x}$$
				- $$=\left(2\cos^2x+x\cdot\cos x+\sin x\cdot\cos^2x\right)\cdot e^{\sin x}$$
				- $$=\left(x+2\cos x+\sin x\cos x\right)\cos x\cdot e^{\sin x}$$
			- $$\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}=\frac{2\cos x}{e^{\sin x}}\cdot\frac{1}{x+2\cos x+\sin x\cos x}\longrightarrow{}_{x\rightarrow\infty}0$$
			- Problem: $g^{\prime}\left(x\right)$ hat für $x\rightarrow\infty$ immer wieder Nullstellen
				- => l'Hospital greift nicht
-