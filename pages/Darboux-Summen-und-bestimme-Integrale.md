reference:: 10b

-
- Definition: **Ober- und Unterintegral**
	- sei $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ beschränkt
	- *Oberintegral*
		- $^{\ast}\int_{a}^{b}\coloneqq\inf\left\lbrace\int_{a}^{b}\psi;\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,f\leq\psi\right\rbrace$
		- $_{\ast}\int_{a}^{b}\coloneqq\sup\left\lbrace\int_{a}^{b}\varphi;\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\right\rbrace$
-
- Beispiel
	- $$f:\left\lbrack0,1\right\rbrack\rightarrow\mathbb{R},f\left(x\right)\coloneqq\left\lbrace_{0,x\notin\mathbb{Q}}^{1,x\in\mathbb{Q}}\right.$$
	- -> effektiv "zwei" Linien, aber keine zwei Punkte auf dem selben x
	- $$^{\ast}\int_0^1f=1\neq0=_{\ast}\int_0^1f$$
-
- Definition: **Riemann Integrierbarkeit**
	- reference:: 10.9
	- Eine beschränkte Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ heißt (Riemann) integrierbar, wenn $\int_{a}^{b}f\coloneqq_{\ast}\int_{a}^{b}f=^{\ast}\int_{a}^{b}f$ gilt
	- $\mathbb{R}\left\lbrack a,b\right\rbrack$: Menge der integrierbaren Funktionen auf [a,b]
-
- Satz: **Einschließung durch Treppenfunktionen**
	- reference:: 10.10
	- Eine Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ ist genau dann integrierbar, wenn es zu jedem $\varepsilon>0$ Treppenfunktionen $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ gibt mit $\varphi\leq f\leq\psi$ und
	- $$\int_{a}^{b}\left(\psi\left(x\right)-\varphi\left(x\right)\right)dx<\varepsilon$$
	- $$=\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx$$
	- Beweis
	  collapsed:: true
		- "=>"
			- seien $f\in\mathbb{R}\left\lbrack a,b\right\rbrack,\varepsilon>0$
			- $$^{\ast}\int_{a}^{b}f=_{\ast}\int_{a}^{b}f$$
			- es gibt ein $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und
			- $$\int_{a}^{b}\varphi\left(x\right)dx>_{\ast}\int_{a}^{b}f\left(x\right)dx-\frac{\varepsilon}{2}$$
				- -> keine obere Schranke
			- $$\int_{a}^{b}\psi\left(x\right)<^{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}$$
				- -> keine untere Schranke
			- $\int_{a}^{b}$ ist linear für Treppenfunktionen
			- $$\Rightarrow\int_{a}^{b}\left(\varphi\left(x\right)-\varphi\left(x\right)\right)dx=\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx$$
			- $$<^{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}-_{\ast}\int_{a}^{b}f\left(x\right)dx+\frac{\varepsilon}{2}$$
			- $$\Rightarrow\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
		- "<="
			- für $\varepsilon>0$ gibt es $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und
			- $$^{\ast}\int_{a}^{b}f\left(x\right)dx-_{\ast}\int_{a}^{b}f\left(x\right)dx\leq\int_{a}^{b}\psi\left(x\right)dx-\int_{a}^{b}\varphi\left(x\right)dx<\varepsilon$$
			- Im Limes $\varepsilon\downarrow0$ folgt $_{\ast}\int_{a}^{b}f\left(x\right)dx=^{\ast}\int_{a}^{b}f\left(x\right)dx$
-
- Korollar:
	- reference:: 10.11
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},c\in\left(a,b\right)$
	- Dann $f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Leftrightarrow f\in\left\lbrack a,c\right\rbrack\text{ und }f\in\mathbb{R}\left\lbrack c,b\right\rbrack$
	- Dann gilt: $\int_{a}^{b}f\left(x\right)dx=\int_{a}^{c}f\left(x\right)dx+\int_{c}^{b}f\left(x\right)dx$
-
- Übung:
	- reference:: 10.12
	- $$\int_{a}^{b}f\left(x\right)dx=\int_{a}^{c}f\left(x\right)dx+\int_{c}^{b}f\left(x\right)dx$$
	- $f:\left\lbrack1,2\right\rbrack\rightarrow\mathbb{R},f\left(x\right)\coloneqq\frac{1}{x}$
	- zZ: $f\in\mathbb{R}\left\lbrack1,2\right\rbrack$
	- Beweis
	  collapsed:: true
		- für $n\in\mathbb{N}:\Delta x\coloneqq\frac{1}{n}$
		- $x_{k}\coloneqq1+k\cdot\Delta x=1+\frac{k}{n}$
		- => $\left(x_{k}\right)_{k=0}^{\infty}\in\mathbb{Z}\left\lbrack1,2\right\rbrack$
		- Für die untere Treppenfunktion:
			- $$a_{k}\coloneqq\frac{1}{x_{k}}=\frac{1}{1+\frac{k}{n}}=\frac{1}{\frac{n+k}{n}}=\frac{n}{n+k}$$
		- Für die obere Treppenfunktion:
			- $$b_{k}\coloneqq\frac{1}{x_{k-1}}=\frac{n}{n+k-1}$$
		- Untersumme:
			- $$\int_{a}^{b}\varphi_{n}=\sum_{k=1}^{n}\frac{n}{n+k}\cdot\frac{1}{n}=\sum_{k=1}^{n}\frac{1}{n+k}=\frac{1}{n+1}+...+\frac{1}{2n}$$
		- Obersumme:
			- $$\int_{a}^{b}\psi_{n}=\sum_{k=1}^{b}\frac{n}{n+k-1}\cdot\frac{1}{n}=\sum_{k=1}^{n}\frac{1}{n+k-1}=\frac{1}{n}+...+\frac{1}{2n-1}$$
		- $$\Rightarrow\int_{a}^{b}\left(\psi_{n}-\varphi_{n}\right)=\frac{1}{n}-\frac{1}{2n}=\frac{1}{2n}\longrightarrow{}_{n\rightarrow\infty}0$$
		- Notiz
			- $$\int_1^2\frac{1}{x}dx=\lim_{n\rightarrow\infty}\sum_{k=1}^{n}\frac{1}{n+k}=\lim_{k\rightarrow\infty}\left(\frac{1}{k+1}+...+\frac{1}{2n}\right)$$
-
- Satz:
	- reference:: 10.13
	- Zu jeder stetigen Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ und jedem $\varepsilon>0$ gibt es Treppenfunktionen $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $\varphi\leq f\leq\psi$ und $\psi-\varphi<\varepsilon$
	- Beweis
		- Übung 7.15 => f ist sogar gleichmäßig stetig
		- => Es gibt ein $\delta=\delta\left(\varepsilon\right)>0\left(\delta\neq\delta\left(x\right)\right)$ mit
		- $$\forall x,y\in\left\lbrack a,b\right\rbrack:\left|x-y\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(y\right)\right|<\frac{\varepsilon}{2}$$
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
- Satz:
	- reference:: 10.14
	- Jede stetige Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ ist integrierbar
	- Beweis
	  collapsed:: true
		- Satz 10.13 => zu $\varepsilon>0$ gibt es Treppenfunktionen $\varphi\leq f\leq\psi$ mit $\psi-\varphi<\frac{\varepsilon}{2\left(b-a\right)}$
		- => $\int_{a}^{b}\left(\psi-\varphi\right)\leq\int_{a}^{b}\frac{\varepsilon}{2\left(b-a\right)}$
		- also $\left(b-a\right)\cdot\frac{\varepsilon}{2\left(b-a\right)}=\frac{\varepsilon}{2}<\varepsilon$
	- Bemerkung
		- Riemann-Summe: $\sum_{k=1}^{n}f\left(\xi_{k}\right)\cdot\left(x_{k}-x_{k-1}\right)\approx\int_{a}^{b}f\left(x\right)dx$
	- Bemerkung
		- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ "stückweise stetig" ist ausreichend
-
- Übung
	- $f:\left\lbrack0,1\right\rbrack\rightarrow\mathbb{R}$ mit $f\left(x\right)=\sin\left(\frac{1}{x}\right)$ für $x\neq0$ und $f\left(0\right)=0$
	- $f\in\mathbb{R}\left\lbrack0,1\right\rbrack$, obwohl bei x=0 "sehr unstetig"
	- Beweis
	  collapsed:: true
		- sei $\varepsilon>0$
		- auf $\left\lbrack\frac{\varepsilon}{5},1\right\rbrack$ ist f stetig, also sogar gleichmäßig stetig
		- => Finde $\varphi\leq f\leq\psi$ auf $\left\lbrack\frac{\varepsilon}{5},1\right\rbrack$ mit $\int_{\frac{\varepsilon}{5}}^1\left(\psi-\varphi\right)<\frac{\varepsilon}{2}$
		- Ergänze $\psi\left(x\right)=1$ und $\varphi\left(x\right)=-1$ auf $\left\lbrack0,\frac{\varepsilon}{5}\right\rbrack$
		- $$\Rightarrow\int_0^1\left(\psi-\varphi\right)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$
-
- [[Linearität-des-Integrals]]
-
- Satz: **Monotonie des Integrals**
	- reference:: 10.16
	- $f,g\in\mathbb{R}\left\lbrack a,b\right\rbrack,f\leq g$
	- Beweis
	  collapsed:: true
		- $$\int_{a}^{b}f=_{\ast}\int_{a}^{b}f=\sup\left\lbrace\int_{a}^{b}\varphi;\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\right\rbrace$$
		- $$\leq\sup\left\lbrace\int_{a}^{b}\varphi;\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq g\right\rbrace$$
		- $$=_{\ast}\int_{a}^{b}g=\int_{a}^{b}g$$
-
- Korollar:
	- reference:: 10.17
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack$ gilt
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|\leq\left(b-a\right)\cdot\left\lbrack\sup_{x\in\left\lbrack a,b\right\rbrack}\left|f\left(x\right)\right|\right\rbrack_{\eqqcolon M}$$
	- Beweis
		- $$\left|\int_{a}^{b}f\left(x\right)dx\right|=\pm\int_{a}^{b}f\left(x\right)dx=\left\lbrack\int_{a}^{b}\left(\pm f\left(x\right)\right)dx\right\rbrack_{\geq M}$$
		- $$\leq\int_{a}^{b}Mdx=M\cdot\left(b-a\right)$$
-
- offene Fragen
  collapsed:: true
	- $$\left|f\right|\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- $$f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
-
- Definition: **Positiv- und Negativteil einer Funktion**
	- reference:: 10.18
	- für $f:\left\lbrack a.b\right\rbrack\rightarrow\mathbb{R}$ heißen $f_{+}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},f_{-}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ mit
	- $$f_{+}\coloneqq\left\lbrace_{0,f\left(x\right)<0}^{f\left(x\right),f\left(x\right)\geq0}\right.,f_{-}\coloneqq\left\lbrace_{-f\left(x\right),f\left(x\right)<0}^{0,f\left(x\right)\geq0}\right.$$
	- der Positiv- bzw. Negativteil von f
	- für $x\in\left\lbrack a,b\right\rbrack:$
	- $$f\left(x\right)=f_{+}\left(x\right)-f_{-}\left(x\right),\left|f\left(x\right)\right|=f_{+}\left(x\right)+f_{-}\left(x\right)$$
-
- Satz:
	- reference:: 10.19
	- $$f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Rightarrow f_{+}\in\mathbb{R}\left\lbrack a,b\right\rbrack,f_{-}\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- Beweis
		- sei $\varepsilon>0,\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\leq\psi,\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$
		- $$\Rightarrow\varphi_{+}\leq f_{+}\leq\psi_{+},\psi_{-}\leq f_{-}\leq\varphi_{-}$$
		- Rechne
			- $$\int_{a}^{b}\left(\psi_{+}-\varphi_{+}\right)\leq\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$$
			- $$\int_{a}^{b}\left(\varphi_{-}-\psi_{-}\right)\leq\int_{a}^{b}\left(-\varphi+\psi\right)<\varepsilon$$
-
- Erinnerung
	- $$\left|a+b\right|\leq\left|a\right|+\left|b\right|,\left|\sum_{k=1}^{n}a_{k}\right|\leq\sum_{k=1}^{n}\left|a_{k}\right|$$
-
- Korollar: **Dreiecksungleichung für Integrale**
	- reference:: 10.20
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack$ ist $\left|f\right|\in\mathbb{R}\left\lbrack a,b\right\rbrack$ und
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|\leq\int_{a}^{b}\left|f\left(x\right)\right|dx$$
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|=\pm\int_{a}^{b}f\left(x\right)dx=\int_{a}^{b}\left(\pm f\left(x\right)\right)dx\leq\int_{a}^{b}\left|f\left(x\right)\right|dx$$
-
- Ziel
	- $$f\cdot g\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- Hilfsmittel:
		- $$f\left(x\right)\cdot g\left(x\right)=\frac14\left(\left(f\left(x\right)+g\left(x\right)\right)^2-\left(f\left(x\right)-g\left(x\right)\right)^2\right)$$
	- Brauche:
		- $$f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Rightarrow f^2\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
-
- Lemma:
	- reference:: 10.21
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack,p\in\left\lbrack1,\infty\right)$ ist $\left|f\right|^{p}\in\mathbb{R}\left\lbrack a,b\right\rbrack$
	- Beweis
	  collapsed:: true
		- o.B.d.A. $\forall x\in\left\lbrack a,b\right\rbrack:0\leq f\left(x\right)\leq1$
			- f: einsetze f durch $\left|f\right|$
			- $\leq1$: teile durch $M\coloneqq\sup_{x\in\left\lbrack a,b\right\rbrack}\left|f\left(x\right)\right|>0$
			- zu $\varepsilon>0$ gibt es $\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack$ mit $0\leq\varphi\leq f\leq\psi\leq1$ und $\int_{a}^{b}\left(\psi-\varphi\right)<\frac{\varepsilon}{p}$
			- Erhalte $0\leq\varphi^{p}\leq f^{p}\leq\psi^{p}\leq1$
			- MWS der Differenzialrechnung: $h\left(t\right)\coloneqq t^{p}$
				- $0\leq h^{\prime}\left(t\right)=p\cdot t^{p-1}\leq p$
			- für $s,t\in\left\lbrack0,1\right\rbrack$ gibt es ein $\xi\in\left\lbrack0,1\right)$ mit
				- $$\frac{s^{p}-t^{p}}{s-t}=h^{\prime}\left(\xi\right)\leq p$$
				- $$\Rightarrow s^{p}-t^{p}\leq p\cdot\left(s-t\right)$$
				- $$\Rightarrow\int_{a}^{b}\left(\psi^{p}-\varphi^{p}\right)\leq p\cdot\int_{a}^{b}\left(\psi-\varphi\right)<p\cdot\frac{\varepsilon}{p}=\varepsilon$$
-
- Übung:
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
- Theorem: [[Mittelwertsatz-der-Integralrechnung]]
-
- Korollar:
	- reference:: 10.24
	- Spezialfall: $w\left(x\right)=1:\forall x\in\left\lbrack a,b\right\rbrack$
	- zu jeder stetigen Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ gibt es ein $\xi\in\left\lbrack a,b\right\rbrack$ mit
	- $$\int_{a}^{b}f\left(x\right)dx=f\left(\xi\right)\cdot\left(b-a\right)$$
-
- Definition: **Gewichtsfunktion**
	- reference:: 10.25
	- $w:\left\lbrack a,b\right\rbrack\rightarrow\left\lbrack0,\infty\right)$ integrierbar mit $\int_{a}^{b}w\left(x\right)dx\neq0$
	- $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ integrierbar
	- $$M_{w}\left(f\right)\coloneqq\frac{1}{\int_{a}^{b}w\left(x\right)dx}\int_{a}^{b}f\left(x\right)w\left(x\right)dx$$
		- heißt das (mit w) gewichtete Mittel von f über [a,b]
	- $$M\left(f\right)\coloneqq\frac{1}{b-a}\int_{a}^{b}f\left(x\right)dx$$
		- heißt der Mittelwert von f über [a,b]
-