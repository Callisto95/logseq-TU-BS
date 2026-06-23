- $K$ Menge, $+,\cdot$ kommutative Verknüpfungen auf K
- Dann heißt $K=(K,+,\cdot)$ ein Körper, wenn
	- $(K,+)$ eine abelsche Gruppe ist
	  logseq.order-list-type:: number
		- $e=0=0_{K}$ (0 des Körpers K; auch einfach 0)
	- das Distributivgesetz gilt
	  logseq.order-list-type:: number
		- $a,b,c\in K:a\cdot(b+c)=ab+ac$
	- $(K,\cdot)$ ist ein Monoid, $e=1=1_{K}$
	  logseq.order-list-type:: number
		- mit $K^{\times}=K\setminus\lbrace0\rbrace$ -> $1\neq0$ (inverses Element von 0 existiert nicht, deswegen keine 0)
- Die Elemente aus K heißen **Skalare** (Wert kann auf Skala abgelesen werden)
- K ist Nullteilerfrei ($a,b\in K:ab\neq0$)
-
- **Korollar** (Regeln im Körper)
	- sei $K=(K,+,\cdot)$
	- $\forall a,b\in K:$
		- $0\cdot a=0$
		  logseq.order-list-type:: number
		- $a\cdot-1=-a$ (*additiv inverse*)
		  logseq.order-list-type:: number
		- $a,b\neq0\Rightarrow ab\neq0$
		  logseq.order-list-type:: number
		- $(-a)^2=a^2$
		  logseq.order-list-type:: number
	- Beweise:
		- $0\cdot a=(0+0)\cdot a=0\cdot a+0\cdot a$ =[$-(0\cdot a)$]=> $0=0\cdot a$
		  logseq.order-list-type:: number
		- $-1\cdot a[+a]=-1\cdot a+1\cdot a=(-1+1)\cdot a=0$
		  logseq.order-list-type:: number
		- *Kontraposition*: Wann ist $ab=0$? -> nur wenn $a=0$ oder $b=0$ (falsche Prämisse)
		  logseq.order-list-type:: number
			- Falls $a\neq0$ gibt es dazu wegen $K^{\times}=K\setminus\lbrace0\rbrace$ ein inverses Element $a^{-1}$ bezüglich der Multiplikation
			- also: $ab=0\Rightarrow a^{-1}ab=a^{-1}\cdot0\Rightarrow b=0$
		- logseq.order-list-type:: number
			- Beispiel: $a=1$: $-1+1=0=[\cdot-1]\Rightarrow(-1)^2+(-1)=0=[+1]\Rightarrow(-1)^2=1=1^2$
			- $(-a)^2=(-1\cdot a)^2=(-1)^2\cdot a^2=a^2$
	- binomische Formeln
		- $2_{K}\coloneqq 1_{K}+1_{K}$ (zwei im Körper \coloneqq  1 im Körper + 1 im Körper)
		- dann gelten für $a,b\in K$:
			- $(a+b)^2=a^2+2_{K}ab+b^2$
			  logseq.order-list-type:: number
			- $(a-b)^2=a^2-2_{K}ab+b^2$
			  logseq.order-list-type:: number
			- $(a+b)(a-b)=a^2-b^2$
			  logseq.order-list-type:: number
-
- 1.25: Beispiel
	- $[2]_6\cdot[3]_6=[6]_6=[0]_6$: solange dies nicht der Fall ist, ist K ein Körper
	- Wenn $p\in\mathbb{N}prim$ ist, dann ist $\mathbb{Z}/p\mathbb{Z}=\mathbb{Z_{p}}$ ein Körper mit p Elementen
		- Bezeichnung: $\mathbb{F}_p\coloneqq \mathbb{Z}_{p}=\mathbb{Z}/p\mathbb{Z}$ (Körper = Field)
		- **Galais-Körper**
		- Gibt auch $\mathbb{F}_4\neq\mathbb{Z}_4$ (4 kein prim)
-
- 1.24: Beispiel
	- $R$ ist Integritätsring (z.B. $R=\mathbb{Z}$)
	- $M=\lbrace(x,y):x\in R,y\in R\setminus\lbrace0\rbrace\rbrace$
	- (1.2) $(x,y)\sim(u,v)\Leftrightarrow xv=uy$ Äquivalenzrelation
	- $Q(R)\coloneqq M/\sim=\lbrace[(x,y)];(x,y)\in M\rbrace$ ()Menge aller Zahlenpaare, die zueinander Äquivalent sind)
		- Menge der Äquivalenzklassen mit
			- (1.3) $[(x,y)]\oplus[(u,v)]\coloneqq [(xv+uy,yv)]$ **!!! uv correct**
			- (1.4) $[(x,y)]\odot[(u,v)]\coloneqq [(xu,yv)]$ (auch $\cdot$ bei allen Multiplikationen verwendbar, Erklärung notwendig)
	- ~> $Q(R)$ ist damit ein Körper, der **Quotientenkörper** von R
		- Beispiel: $R=\mathbb{Z}\Rightarrow Q(\mathbb{Z})=\mathbb{Q}$
-