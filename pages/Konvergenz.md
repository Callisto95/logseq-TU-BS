- Es seien $\left(a_{k}\right)\subseteq\mathbb{R}$ eine Folge und $a\in\mathbb{R}$
- Wenn $\forall\epsilon>0:\exists n\in\mathbb{N}:\forall k\geq n:\left|a_{k}-a\right|<\epsilon$ gilt, heißt a der *Grenzwert* (oder *Limes*) von $\left(a_{k}\right)$
	- Notation
	- $$\lim_{k\rightarrow\infty}a_{k}=a\text{ oder }a\longrightarrow{}_{k\rightarrow\infty}a$$
- Wenn eine Folge $\left(a_{k}\right)$ einen Grenzwert besitzt, dann heißt sie **konvergent**, andernfalls **divergent**
	- $\left(a_{k}\right)$ konvergiert / divergiert
-
- $$\forall\epsilon>0:\exists s\in\mathbb{R},s>0:\forall k\in\mathbb{N}:\left(k\geq s\Rightarrow\left|a_{k}-a\right|<\epsilon\right)$$
- Beispiele
	- Konstante Folge
	  logseq.order-list-type:: number
	  collapsed:: true
		- Es sei $\left(a_{k}\right)\subseteq\mathbb{R}$ gegeben durch $a_{k}:=1$
		- Dann gilt $a_{k}\longrightarrow{}_{k\rightarrow\infty}1$
		- Beweis
			- sei $\epsilon>0$
			- wähle $s:=1$ als "Schwellenwert"
			- für $k\in\mathbb{N},k\geq1$ gilt:
			- $\left|a_{k}-1\right|=\left|1-1\right|=0<\epsilon$
			- (Abstand von $a_{k}$ zum Schwellenwert)
	- Bruchfolge
	  logseq.order-list-type:: number
	  collapsed:: true
		- $\left(a_{k}\right)\subseteq\mathbb{R}:a_{k}=\frac{1}{k}$
		- Behauptung: $\lim_{k\rightarrow\infty}\frac{1}{k}=0$
		- Beweis
			- sei $\epsilon>0$
			- Gesucht: Schwelle $s=s\left(\epsilon\right):k\geq s\Rightarrow\left|a_{k}-0\right|<\epsilon$
			- => $\left|\frac{1}{k}-0\right|=\left|\frac{1}{k}\right|=\frac{1}{k}<\epsilon$: ab wann gilt $\frac{1}{k}<\epsilon$
			- Überlegung: $\frac{1}{k}<\epsilon\Leftrightarrow\frac{1}{\epsilon}<k$
			- Wähle $s\left(\epsilon\right):=\frac{1}{\epsilon}+1$
			- Für $k\geq s=\frac{1}{\epsilon}+1$ ist $\left|a_{k}-0\right|=\frac{1}{k}<\epsilon$
	- Alternierende Folge
	  logseq.order-list-type:: number
	  collapsed:: true
		- $\left(a_{k}\right)\subseteq\mathbb{R}:=\left(-1\right)^{k}$
		- Behauptung: $\left(a_{k}\right)$ ist divergent
		- zZ: $\neg\left(\exists a\in\mathbb{R}:\forall\epsilon>0:\exists n\in\mathbb{N}:\forall k\geq n:\left|a_{k}-a\right|<\epsilon\right)$
		- $\Leftrightarrow\forall a\in\mathbb{R}:\exists\epsilon>0:\forall n\in\mathbb{N}:\exists k\geq n:\left|a_{k}-a\right|\geq\epsilon$
		- Idee: "Schlauch" mit $\epsilon=\frac12$ und verschiebe diesen
			- Sei $a\in\mathbb{R}$ (potentieller Grenzwert)
			- Wähle $\epsilon_0:=\frac12>0$
			- Dann: für $n\in\mathbb{N}$ gilt:
			- $2=\left|a_{n+1}-a_{n}\right|=\left|a_{n+1}-a+a-a_{n}\right|=\left|\left(a_{n+1}-a\right)+\left(a-a_{n}\right)\right|\leq\left|a_{n+1}-a\right|+\left|a-a_{n}\right|$
			- Annahme: $\left|a_{n+1}-a\right|<\frac12\land\left|a_{n}-a\right|<\frac12$
			- -> $\left|a_{n+1}-a\right|+\left|a-a_{n}\right|<\frac12+\frac12=1$
			- => $1=2$
-
- Übung 2.13
  collapsed:: true
	- $\lim_{k\rightarrow\infty}\frac{k+1}{k}=1$
	  logseq.order-list-type:: number
		- sei $\epsilon>0$
		- zZ: $\exists s=s\left(\epsilon\right)\in\left(0,\infty\right):\forall k\geq s:\left|\frac{k+1}{k}-1\right|<\epsilon$
		- Rechne: $\frac{k+1}{k}-1=\frac{k+1}{k}-\frac{k}{k}=\frac{k+1-k}{k}=\frac{1}{k}$
		- ab wann $\frac{1}{k}<\epsilon\Leftrightarrow k>\frac{1}{\epsilon}$
		- Wähle $s=s\left(e\right):=\frac{1}{\epsilon}$
	- $\lim_{k\rightarrow\infty}\frac{1}{\sqrt{k}}=0$
	  logseq.order-list-type:: number
		- sei $\epsilon>0$
		- zZ: $\exists s=s\left(\epsilon\right)\in\left(0,\infty\right):\forall k\in\mathbb{N}:$
		- $k\geq s\Rightarrow\left|\frac{1}{\sqrt{k}}-0\right|<0\Leftrightarrow\frac{1}{\sqrt{k}}<0$
		- für $k\in\mathbb{N}$ gilt:
		- $$\frac{1}{\sqrt{k}}<\epsilon\Leftrightarrow\sqrt{k}>\frac{1}{\epsilon}\Leftrightarrow_{\sqrt{.}}^{\left(.\right)^2}k>\frac{1}{\epsilon^2}=:s$$
		- Wähle $s\left(\epsilon\right):=\frac{1}{\epsilon^2}+1$
-
- **Nullfolgen**
  collapsed:: true
	- Folgen, die gegen 0 konvergieren
	- => $\left(a_{k}\right)\subseteq\mathbb{R}$ heißt Nullfolge, wenn $\lim_{k\rightarrow\infty}a_{k}=0$
-
- **Bälle und Umgebung**
	- für $x\in\mathbb{R},r\in\left(0,\infty\right)$ heißt das Intervall $\mathbb{N}$
-