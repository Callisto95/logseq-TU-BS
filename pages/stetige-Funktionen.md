- sei $f:\mathbb{R}\rightarrow\mathbb{R}$
	- Input x -> Output f(x)
- Probleme
	- x Fehlerbefreit?
	- Was passiert mit f(x)?
	- genauigkeit bei $x=\sqrt2,x=\pi$: "Exakte Eingabe"
- Möchte: Wenn $x\approx y\Rightarrow f\left(x\right)\approx f\left(y\right)$
-
- Definition: **Stetigkeit**
	- reference:: 5.a
	- sei $f:\mathbb{R}\rightarrow\mathbb{R}$ eine (partielle) Funktion
	- d.h. $D\coloneqq \text{Dom}f\subseteq\mathbb{R}$ und $f:D\rightarrow\mathbb{R}$
	- für $v\in D$ heißt f *stetig in v*, wenn $\forall\varepsilon>0:\exists\delta>0:\forall x\in D:\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|<\varepsilon$
	  logseq.order-list-type:: number
		- $\varepsilon>0$: Fehler im Output (y-Ball / y-Variation)
		- $\delta>0$: ausreichende Präzision im Input (x-Ball / x-Variation)
	- Wenn f in jedem $v\in D$ stetig ist, dann heißt stetig (f ist eine stetige Funktion)
	  logseq.order-list-type:: number
		- $f\in C\left(D\right)$, f aus der Klasse der stetigen Funktionen (C: continous)
	- Beispiel
	  collapsed:: true
		- $f:\mathbb{R}\rightarrow\mathbb{R}:f\left(x\right)=42$
		  logseq.order-list-type:: number
		  collapsed:: true
			- sei $\varepsilon>0$, jedes $\delta>0$ erfüllt Stetigkeit
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)=x$
		  logseq.order-list-type:: number
		  collapsed:: true
			- zu $\varepsilon>0$ wähle $\delta\coloneqq \varepsilon$
			- $$\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|=\left|x-v\right|<\delta=e$$
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq 2x$
		  logseq.order-list-type:: number
		  collapsed:: true
			- zu $\varepsilon>0$ wähle $\delta\coloneqq \frac{\varepsilon}{2}$
			- $\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|=\left|2x-2v\right|=2\left|x-v\right|<2\cdot\delta=2\cdot\frac{\varepsilon}{2}=\varepsilon$
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)=x^2$
		  logseq.order-list-type:: number
		  collapsed:: true
			- Stetigkeit in $v\in\mathbb{R}:x=v+h$
			- Ziel: $\left|f\left(v\right)-f\left(v+h\right)\right|<\varepsilon$
			  collapsed:: true
				- $=\left|v^2-\left(v+h\right)^2\right|=\left|2vh-h^2\right|=\left|h\right|\cdot\left|2v+h\right|\Rightarrow\left\lbrack<\delta\right\rbrack\cdot\left\lbrack<^{?}\varepsilon\right\rbrack$
			- Idee
			  collapsed:: true
				- $\left|2v+h\right|\cdot\delta<\varepsilon\Rightarrow\delta=\frac{\varepsilon}{\left|2v+h\right|}$
				- Notiz: $\left|2v+h\right|\leq\left|2v\right|+\left|h\right|\leq^{\left|h\right|\leq1}2\left|v\right|+1$
				- Wähle $\delta=\delta\left(v,\varepsilon\right)\coloneqq \min\left\lbrace\frac{1}{2\left|v\right|+1}\varepsilon,1\right\rbrace$
				- => Für $\left|h\right|<\delta:\left|f\left(v\right)-f\left(v+h\right)\right|<\delta\cdot\left|2v+h\right|\leq\frac{1}{2\left|v\right|+1}\varepsilon\cdot\left|2v+h\right|\leq^{\text{wegen }2\left|v\right|+1\leq1\land\left|2v+h\right|\leq1}\varepsilon$
-
- Definition: **Lipschitz-Stetigkeit**
	- reference:: 5.2
	- Eine Funktion $f:\mathbb{R}\rightarrowtail\mathbb{R}$ heißt Lipschitz-Stetig, wenn:
	- $$\exists L\in\left\lbrack0,\infty\right):\forall x,y\in\text{Dom}f:\left|f\left(x\right)-f\left(y\right)\right|\leq L\cdot\left|x-y\right|$$
-
- Übungen: f lipschitz => f stetig
  collapsed:: true
	- 5.3
		- Behauptung: f lipschitz => f stetig
		- Beweis
			- sei $\varepsilon>0,x\in\text{Dom}f$
			- zZ: $\exists\delta=\delta\left(\varepsilon,x\right)>0:\forall y\in\text{Dom}f:\left|x-y\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(y\right)\right|<\varepsilon$
			- Rechne: $\left|f\left(x\right)-f\left(y\right)\right|\leq L\cdot\left|x-y\right|<^{?}\varepsilon$
			- Für $\left|x-y\right|<\delta$ ist $\left|f\left(x\right)-f\left(y\right)\right|\leq L\cdot\left|x-y\right|<L\cdot\frac{1}{L+1}\varepsilon<\varepsilon$
	- 5.4
		- a) Für $c>0$ ist die Funktion $f:\left\lbrack c,\infty\right)\rightarrow\mathbb{R,f\left(x\right)}\coloneqq \sqrt{x}$ lipschitz-stetig
			- für $x,y\in\left\lbrack c,\infty\right)$ betrachte:
			- $$f\left(x\right)-f\left(y\right)=\sqrt{x}-\sqrt{y}=\left\lbrack\text{3. binomische Formel}\right\rbrack=\frac{x-y}{\sqrt{x}+\sqrt{y}}=\frac{x-y}{\geq\sqrt{2c}}$$
			- $$\Rightarrow\left|f\left(x\right)-f\left(y\right)\right|=\frac{1}{\sqrt{x}+\sqrt{y}}\cdot\left|x-y\right|\leq L\cdot\left|x-y\right|$$
			- mit $\frac{1}{\sqrt{x}+\sqrt{y}}\leq\frac{1}{\sqrt{2c}}$ wähle $L\coloneqq \frac{1}{\sqrt{2c}}$
			- $L=\frac{1}{2\sqrt{c}}\longrightarrow{}_{c\rightarrow\infty}\infty$
		- b) $g:\left\lbrack0,\infty\right)\rightarrow\mathbb{R}:g\left(x\right)\coloneqq \sqrt{x}$ ist stetig, aber nicht lipschitz
			- Annahme: g wäre lipschitz mit Konstante $L\geq0$
			- $$\Rightarrow\forall x,y\in\left\lbrack0,\infty\right):x\neq y\Rightarrow\frac{\left|\sqrt{x}-\sqrt{y}\right|}{\left|x-y\right|}\leq L$$
			- für $y\coloneqq 0,n\in\mathbb{N}:x\coloneqq \frac{1}{n^2}$ ergibt
			- $\frac{\frac{1}{n}-0}{\frac{1}{n^2}-0}=n\leq L$ => unbeschränktheit (Archimedes): unmöglich
			- aber Stetigkeit: g ist in allen x>0 stetig
			- zZ: g ist in x=0 stetig
				- sei $\varepsilon>0$
				- Ziel: Finde $\delta>0$ mit $\left|y-x\right|<\delta\Rightarrow\left|\sqrt{x}-\sqrt{y}\right|<\varepsilon$
				- da x=0: $\sqrt{y}<\varepsilon\Leftrightarrow y<\varepsilon^2$
				- Also: $\delta\coloneqq \varepsilon^2$
-
- Satz: **Stetigkeit von Folgen**
	- reference:: 5.5
	- $f:\mathbb{R}\rightarrowtail\mathbb{R},v\in\text{Dom}f$
	- Behauptung: f ist genau dann in v stetig, wenn
	- $$\forall\left(x_{k}\right)\subseteq\text{Dom}f:\left(x_{k}\longrightarrow{}_{k\rightarrow\infty}v\Rightarrow f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)\right)$$
	- Beweis
	  collapsed:: true
		- "=>"
			- sei f stetig in v
			- sei $\left(x_{k}\right)\subseteq\text{Dom}f$ eine beliebige Folge mit $x_{k}\longrightarrow{}_{k\rightarrow\infty}v$
			- zZ: $f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)$
			- sei $\varepsilon>0$, zZ: $\exists n\in\mathbb{N}:\forall k\geq n:\left|f\left(x_{k}\right)-f\left(v\right)\right|<\varepsilon$
			- f stetig in v => es gibt eine $\delta=\delta\left(e\right)>0$ mit $\forall x\in\text{Dom}f:\left|x-v\right|<\delta\Rightarrow\left|f\left(x\right)-f\left(v\right)\right|<\varepsilon$
			- Wegen $x_{k}\longrightarrow{}_{k\rightarrow\infty}v$ gibt es zu diesem $\delta>0$ ein $n=n\left(\delta\right)=n\left(\delta\left(\varepsilon\right)\right)\in\mathbb{N}$ mit $\forall k\geq n:\left|x_{k}-v\right|<\delta$
			- => für $k\geq n:\left|f\left(x_{k}\right)-f\left(v\right)\right|<\varepsilon$
			- => $f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)$
		- "<="
			- Angenommen sei f in $v\in\text{Dom}f$ unstetig
			- zZ: Es gibt eine Folge $\left(x_{k}\right)\subseteq\text{Dom}f$ mit
			- $x_{k}\longrightarrow{}_{k\rightarrow\infty}v$, aber nicht $f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)$
			- f ist unstetig in v => $\exists\varepsilon_0>0:\forall k\in\mathbb{N}:\exists x_{k}\in\text{Dom}f:\left|x_{k}-v\right|<\frac{1}{k}\land\left|f\left(x_{k}\right)-f\left(v\right)\right|\geq\varepsilon_0$
				- dabei $\forall\delta>0,\delta\coloneqq \frac{1}{k}$
			- => $\left|x_{k}-v\right|<\frac{1}{k}\longrightarrow{}_{k\rightarrow\infty}0\Rightarrow x_{k}\longrightarrow{}_{k\rightarrow\infty}v$
			- aber nicht $f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)$
-
- Beispiele
  collapsed:: true
	- 5.6
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq x^2$ ist stetig:
		- Beweis
			- Für $v\in\mathbb{R,\left(x_{k}\right)}\subseteq\mathbb{R},x_{k}\longrightarrow{}_{k\rightarrow\infty}v$ ist $f\left(x_{k}\right)=x_{k}^2=x_{k}\cdot x_{k}\longrightarrow{}_{k\rightarrow\infty}v\cdot v=v^2=f\left(v\right)$
	- 5.7
		- $\text{sign}:\mathbb{R}\rightarrow\mathbb{R},\text{sign}\left(x\right)\coloneqq \left\lbrace1:x>0\right.;0:x=0;-1<0$
		- sign ist in jedem $v\in\mathbb{R}\setminus\left\lbrace0\right\rbrace$ stetig
		- sign ist in v=0 unstetig
			- $x_{k}\coloneqq -\left(-1\right)^{k}\cdot\frac{1}{k}\longrightarrow{}_{k\rightarrow\infty}0$
			- $\text{sign}\left(x_{k}\right)=-\left(-1\right)^{k}$ divergiert
	- 5.8
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)\coloneqq \left(\text{sign}\left(x\right)\right)^2$
		- f ist in allen $v\neq0$ stetig
		- aber: $x_{k}\coloneqq \frac{1}{k}\longrightarrow{}_{k\rightarrow\infty}0,f\left(x_{k}\right)=1\longrightarrow{}_{k\rightarrow\infty}1\neq f\left(0\right)=0$
	- 5.9
		- $f,g:\mathbb{R}\rightarrowtail\mathbb{R}$ partielle funktionen
		- wenn f und g in $v\in\text{Dom}f\cap\text{Dom}g$ stetig sind, dann ist auch $f+g:\text{Dom}f\cap\text{Dom}g\rightarrow\mathbb{R},\left(f+g\right)\left(x\right)\coloneqq f\left(x\right)+g\left(x\right)$ in v stetig
		  logseq.order-list-type:: number
			- sei $\left(x_{k}\right)\subseteq\text{Dom}\left(f+g\right)$ mit $x_{k}\longrightarrow{}_{k\rightarrow\infty}v$
			- => $\left(f+g\right)\left(x_{k}\right)=f\left(x_{k}\right)+g\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)+g\left(v\right)=\left(f+g\right)\left(v\right)$
		- wenn f und g in $v\in\text{Dom}f\cap\text{Dom}g$ stetig sind, dann ist auch $f\cdot g:\text{Dom}f\cap\text{Dom}g\rightarrow\mathbb{R},\left(f\cdot g\right)\left(x\right)\coloneqq f\left(x\right)\cdot g\left(x\right)$ in v stetig
		  logseq.order-list-type:: number
		- $v\in\text{Dom}f$ stetig und $f\left(v\right)\neq0$
		  logseq.order-list-type:: number
			- => auch $\frac{1}{f}:\left\lbrace x\in\text{Dom}f;f\left(x\right)\neq0\right\rbrace\rightarrow\mathbb{R}$
			- $\left(\frac{1}{f}\right)\left(x\right)\coloneqq \frac{1}{f\left(x\right)}$ ist in v stetig
	- idk
		- $f:\mathbb{R}\rightarrow\mathbb{R},f\left(x\right)=x$ und $g:\mathbb{R}\rightarrow\mathbb{R},g\left(x\right)=c$ stetig
	- 5.10: für $n\in\mathbb{N}_0$ und Koeffizienten $a_0,...,a_{n}\in\mathbb{R}$ heißt $p:\mathbb{R}\rightarrow\mathbb{R},p\left(x\right)\coloneqq \sum_{k=0}^{n}a_{k}x^{k}$ eine Polynomfunktion
		- => *Jede Polynomfunktion ist stetig*
	- 5.11: Ganzrationale Funktionen
		- Für Polynomfunktionen $p,q:\mathbb{R}\rightarrow\mathbb{R}$ wird durch $\frac{p}{q}\left(x\right)\coloneqq \frac{p\left(x\right)}{q\left(x\right)}$ mit $x\in\text{Dom}\frac{p}{1}\coloneqq \left\lbrace x\in\mathbb{R},q\left(x\right)\neq0\right\rbrace$ eine (partielle) Funktion definiert
		- Jede solche Funktion ist in ihrem Definitionbereich stetig und heißt Ganzrationale Funktion
-
- Satz:
	- reference:: 5.12
	- $f:\mathbb{R}\rightarrowtail\mathbb{R},g:\mathbb{R}\rightarrowtail\mathbb{R},\text{Ran}\left(f\right)\subseteq\text{Dom}\left(g\right)$
	- Verkettung: $g\circ f:\text{Dom}\left(f\right)\rightarrow\mathbb{R},x\mapsto\left(g\circ f\right)\left(x\right)\coloneqq g\left(f\left(x\right)\right)$
	- Wenn f in $v\in\text{Dom}\left(f\right)$ und g in $w\coloneqq f\left(v\right)$ stetig ist, dann ist $g\circ f$ in v stetig
	- Beweis
		- sei $\left(x_{k}\right)\subseteq\text{Dom}\left(f\right)$ mit $\lim_{k\rightarrow\infty}x_{k}=v$
		- zZ: $g\left(f\left(x_{k}\right)\right)\longrightarrow{}_{k\rightarrow\infty}g\left(f\left(v\right)\right)=g\left(w\right)$
		- f in v stetig => mit $y_{k}\coloneqq f\left(x_{k}\right)$ konvergiert $y_{k}=f\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}f\left(v\right)=w$
		- g in $w=f\left(v\right)$ stetig => $g\left(y_{k}\right)\longrightarrow{}_{k\rightarrow\infty}g\left(w\right)$
		- => $\left(g\circ f\right)\left(x_{k}\right)\longrightarrow{}_{k\rightarrow\infty}\left(g\circ f\right)\left(v\right)$
			- Also:
			- $$g\left(f\left(v\right)\right)=g\left(f\left(\lim_{k\rightarrow\infty}x_{k}\right)\right)=g\left(\lim_{k\rightarrow\infty}f\left(x_{k}\right)\right)=\lim_{k\rightarrow\infty}g\left(f\left(x_{k}\right)\right)$$
-