- Grundlagen:
	- [[Zahlenbereiche]]
	- [[Mengen-mit-Verknüpfung]]
	- [[Äquivalenzrelation]]
	- [[Restklasse]]
	- [[Äquivalenzklasse]]
	- [[Einheitengruppe]]
	-
	-
	- **Potenzmenge**: $2^{M}$: Menge aller Teilmengen
	- **Kardinalität**: $|M|$: Anzahl der Elemente in $M$
	-
	- **Einheitengruppe**:
		- alle multiplikativ invertierbare Elemente
		- Monoid (M, *) mit neutralen Element $e \in M$
		- $M^x := \{g \in M: \exists \widetilde{g} \in M: g \ast \widetilde{g} = e\}$ Einheitengruppe von M
	-
	- Abbildungen
		- sei M eine Menge
		- Dann wird die Menge $Map(M,M)$ aller Abbildungen von M nach M durch die Verkettung als Verknüpfung zu einem Monoid
		- neutrales Element $I_{M}$, $\forall x\in M:I_{M}(x)=x$
		- Einheitengruppe des neutralen Elements / der Menge (> undeutlich **???**)
			- $Perm\ M:=(Map(M,M))^{\times}=\lbrace f:M\rightarrow M\rbrace$, wobei f *bijektiv* ist
			- ist mit der gleichen Verknüpfung eine (i.A. nicht abelsche) Gruppe
			- = Permutationsgruppe (bzw. symmetrische Gruppe) von M
		- Beispiel
			- $\mathbb{Z}\subseteq\mathbb{Q}$
			- beide Mengen bilden mit der Addition eine Gruppe
		-
	- Einheitsgruppen:
		- Permutationen: $Perm \, M = Map(M, M)^x = \{f: M -> M, f \  bijektiv / eindeutig\}$
			- $f: x_1 \mapsto x_1, x_2 \mapsto x_4, x_y \mapsto x_z$
			- $\mathbb{F}: x_1 \mapsto x_1 ,x_4 \mapsto x_2, x_z \mapsto x_y$
				- nicht kommutativ
	- Untergruppen:
		- G = (G, $\ast$) Gruppe, U $\leq$ G Teilmenge
		- Wenn U mit $\ast$ (bzw. ihrer Einschränkung auf U) selbst eine Gruppe ist, dann heißt U Untergruppe von G, bzw. U $\leq$ G
		- triviale Untergruppen:
			- $\{e\} \leq G$
			- $G \leq G$
			- bei beiden Fällen in der selben Gruppe: einfache Gruppe
				- Bsp: $n\mathbb{Z} \leq \mathbb{Z}$ Untergruppe von $(\mathbb{Z}, +)$
				- $n\mathbb{Z}$ als Teilmenge von $(\mathbb{Z}, \ast)$  mit Untergruppe
					- aber $1 ! \in n\mathbb{Z}$ für z $\geq$ 2, kein Monoid
		- Untergruppenkriterium
			- (G, $\ast$), Teilmenge U $\leq$ G ist genau dann Untergruppe von G, wenn $U \neq \varnothing$ und $\forall u, v \in U: u \ast v^{-1} \in U$
			- Beweis:
				- =>: klar
				- <=: weiterhin assoziativ
					- $U \neq \varnothing => \exists u \in U =[v=u]=> u \ast u^{-1} \in U$, d.h. $e \in U$
					- d.h. U Monoid mit $e \in G$
					- G Gruppe, d.h. $v \in U \leq G$ gibt es $v^{-1} \in G$ erfüllt $v \ast v^{-1} = e$
						- durch v=u: $e,v \in U$ => $e \ast v^{-1} = v^{-1} \in U$
						- =>d.h. (U, $\ast$) Gruppe, bzw. $U \leq G$
		- Herstellung neuer Gruppen:
			- (G, $\ast$), (H, *) Gruppen
			- G x H mit (G x H) x (G x H) -> (G x H), $((g_1, h_1), (g_2, h_2)) \mapsto (g_1 \ast g_2, h_1 \ast h_2)$
				- $(g_1, h_1)$ \in G x H
				-
- Bedeutungen:
	- trivial:
		- ein Fall, der keine Erklärung braucht
-
-
- **Ringe**
	- $(R,+,\cdot)$: Menge und zwei Verknüpfungen
	- Es ist ein RIng, wenn
		- Magma $(R,+)$ ist eine abelsche Gruppe; $e$ wird mit 0 bezeichnet
		- das Distributivgesetz gilt ($a,b,c\in R:a\cdot(b+c)=ab+ac$ und $(a+b)\cdot c=ac+bc$)
		- Magma $(R,\cdot)$ ist eine Halbgruppe
	- **besondere Ringe**
		- Wenn $(R,\cdot)$ kommutativ ist, dann ist der Ring ein *kommutativer Ring*
		- Wenn $(R,\cdot)$ ein Monoid ist, dann wird sein Element als 1 bezeichnet (= die Eins des Rings). Der Ring ist ein *unitärer Ring*
			- $R^{\times}:=\lbrace r\in R:\exists r^{-1}\in R:r\cdot r^{-1}=1\rbrace$ ist die Einheitengruppe des unitären Rings
			- Die Elemente von $R^{\times}$ heißen Einheiten
		- Wenn $R$ ein kommutativer, unitärer Ring mit der Eigenschaft $\forall x,y\in R\setminus\lbrace0\rbrace:x\cdot y\neq0$, dann ist R ein *Integritätsring*
			- $R$ ist nullteilerfrei
			- Beispiel: $\mathbb{Z}$ mit Einheitengruppe $R^{\times}=\lbrace1,-1\rbrace$
			- $x,y,z\in R:x\neq0$, dann $xy=xz\Rightarrow y=z$
	- Konstruktion der rationalen Zahlen
		- $M:=\lbrace(x,y)\in\mathbb{Z^2}:y\neq0\rbrace$ seien durch die Relation $(x,y)\sim(u,v):\Leftrightarrow xv\sim uy$
		- TODO Zeige, dass $\sim$ eine Äquivalenzrelation ist
		  :LOGBOOK:
		  CLOCK: [2024-10-22 Tue 20:13:59]--[2024-10-22 Tue 20:14:00] =>  00:00:01
		  CLOCK: [2024-10-22 Tue 20:14:00]--[2024-10-22 Tue 20:14:01] =>  00:00:01
		  CLOCK: [2024-10-22 Tue 20:14:10]--[2024-10-22 Tue 20:14:11] =>  00:00:01
		  :END:
			- => Unformung $xv=uy\rightarrow\frac{x}{y}=\frac{u}{v}$
			- Reflexivität für $(x,y)\in M$ gilt $x\cdot y=y\cdot x$
				- deswegen gilt $(x,y)\sim(x,y)$
			- Symmentrie
				- $(x,y)\in M$ und $(u,v)\in M$ mit $(x,y)\sim(u,v)$, dann gilt $xv=uy$ also auch $uy=xv$, somit auch $(u,v)\sim(x,y)$
			- Transitivität
				- $(x,y),(u,v),(s,t)\in M$
				- $(x,y)\sim(u,v)$ und $(u,v)\sim(s,t)$ = $xv=uy$ und $ut=sv$
				- $(\ast)$ -> dann $xv=uy$ und $(x,y)\sim(s,t)$
				- zu zeigen ist $(x,y)\sim(s,t),xt=sy$
				- --
				- $(\ast\ast)$ $xv\cdot ut=uy\cdot sv$
					- Fall: $u=0$: aus $(\ast)$ ergibt sich $x=0$ und $s=0$, da v und y nicht 0 sein können (da sie der Nenner sind -> Äquivalenzrelation [Umformung zu Brüchen])
						- Dann ist $xt=0=sy$
					- Fall: $u\neq0$: Nullteilerfreiheit fordert $uv\neq0$
						- $(\ast\ast)$ $uvxt=uvsy$ =[$uv$ kürzen]=> $xt=sy$
				- ==> ist eine Äquivalenzrelation
	- Addition rationaler Zahlen
		- $M,\sim$ wie bei der Konstruktion rationaler Zahlen
		- $\mathbb{Q}:=M/\sim=\lbrace[x,y];x,y\in M\rbrace$ ist die Menge der Äquivalenzklassen bezüglich der Relation
		- Untersuche, durch welche Folgende Ansätze eine Verknüpfung auf den rationalen Zahlen $\mathbb{Q}$ definiert wird
			- a: $[(x,y)]\oplus[(u,v)]:=[(x+u),(y+v)]$ == $\frac{x}{y}\oplus\frac{u}{v}:=\frac{x+u}{y+v}$ => nicht Wahr (so werden nicht Brüche addiert)
				- $\frac12+\frac23=[(1,2)]\oplus[(2,3)]=[(1+2,2+3)]=[(3,5)]$
				  id:: 6716311d-ac39-4f59-a11a-32268d5bcfcd
				- $\frac24+\frac69=[(2,4)]\oplus[(6,9)]=[(2+6,4+9)]=[(8,13)]$
					- $[(3,5)]\neq[(8,13)]$
			- b: $[(x,y)]\#[(u,v)]:=[(xv+uy,yv)]$
				- $\frac{x}{y}\#\frac{u}{v}:=\frac{xv+uy}{yv}$
				- $[(x,y)]=[(x^{\prime},y^{\prime})]$, sodass $xy^{\prime}=x^{\prime}y$ und $[(u,v)]=[(u^{\prime},v^{\prime})]$, sodass $uv^{\prime}=u^{\prime}v$
				- zeige, dass $[(x,y)]\#[(u,v)]=[(x^{\prime},y^{\prime})]\#[(u^{\prime},v^{\prime})]$
					- $(xv+uy,yv)\sim(x^{\prime}v^{\prime}+u^{\prime}y^{\prime},y^{\prime}v^{\prime})$
					- $xvy^{\prime}v^{\prime}+uyy^{\prime}v^{\prime}=x^{\prime}v^{\prime}yv+u^{\prime}y^{\prime}yv$
					- $(\ast)$ $xy^{\prime}vv^{\prime}=x^{\prime}yvv^{\prime}$ => einsetzen in ^, wodurch die Gleichung erfüllt ist
				- ===> # ist eine Verknüpfung auf $\mathbb{Q}$
-
- TODO $(x,y)=[\frac{x}{y}]=\lbrace(u,v);(u,v)\sim(x,y)\rbrace==\frac{x}{y}=\frac{u}{v}==xv=uy==\frac{x}{y}\cdot\frac{u}{v}==\frac{xu}{yu}$
- TODO $\frac{x}{y}+\frac{u}{v}==\frac{xv+uy}{yv}$ repräsentatenunabhängig; $yv\neq0$ -> Nullteilerfreier Ring
- TODO $(x,y)=\frac{x}{y}$
- TODO $M/\sim=M\ mod\sim$
-
- Möchte
  id:: 6718f53b-bba2-44d3-8925-6a5711a304c5
	- $ax=b$ noch x lösen
	- -> $\cdot a^{-1}\rightarrow x=a^{-1}b$
-
- **Körper**
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
		- *Konraposition*: Wann ist $ab=0$? -> nur wenn $a=0$ oder $b=0$ (falsche Prämisse)
		  logseq.order-list-type:: number
			- Falls $a\neq0$ gibt es dazu wegen $K^{\times}=K\setminus\lbrace0\rbrace$ ein inverses Element $a^{-1}$ bezüglich der Multiplikation
			- also: $ab=0\Rightarrow a^{-1}ab=a^{-1}\cdot0\Rightarrow b=0$
		- logseq.order-list-type:: number
			- Beispiel: $a=1$: $-1+1=0=[\cdot-1]\Rightarrow(-1)^2+(-1)=0=[+1]\Rightarrow(-1)^2=1=1^2$
			- $(-a)^2=(-1\cdot a)^2=(-1)^2\cdot a^2=a^2$
	- binomische Formeln
		- $2_{K}:=1_{K}+1_{K}$ (zwei im Körper := 1 im Körper + 1 im Körper)
		- dann gelten für $a,b\in K$:
			- $(a+b)^2=a^2+2_{K}ab+b^2$
			  logseq.order-list-type:: number
			- $(a-b)^2=a^2-2_{K}ab+b^2$
			  logseq.order-list-type:: number
			- $(a+b)(a-b)=a^2-b^2$
			  logseq.order-list-type:: number
-
- 1.24: Beispiel
	- $R$ ist Integritätsring (z.B. $R=\mathbb{Z}$)
	- $M=\lbrace(x,y):x\in R,y\in R\setminus\lbrace0\rbrace\rbrace$
	- (1.2) $(x,y)\sim(u,v)\Leftrightarrow xv=uy$ Äquivalenzrelation
	- $Q(R):=M/\sim=\lbrace[(x,y)];(x,y)\in M\rbrace$ ()Menge aller Zahlenpaare, die zueinander Äquivalent sind)
		- Menge der Äquivalenzklassen mit
			- (1.3) $[(x,y)]\oplus[(u,v)]:=[(xv+uy,yv)]$ **!!! uv correct**
			- (1.4) $[(x,y)]\odot[(u,v)]:=[(xu,yv)]$ (auch $\cdot$ bei allen Multiplikationen verwendbar, Erklärung notwendig)
	- ~> $Q(R)$ ist damit ein Körper, der **Quotientenkörper** von R
		- Beispiel: $R=\mathbb{Z}\Rightarrow Q(\mathbb{Z})=\mathbb{Q}$
-
- 1.25: Beispiel
	- $[2]_6\cdot[3]_6=[6]_6=[0]_6$: solange dies nicht der Fall ist, ist K ein Körper
	- Wenn $p\in\mathbb{N}prim$ ist, dann ist $\mathbb{Z}/p\mathbb{Z}=\mathbb{Z_{p}}$ ein Körper mit p Elementen
		- Bezeichnung: $\mathbb{F}_p:=\mathbb{Z}_{p}=\mathbb{Z}/p\mathbb{Z}$ (Körper = Field)
		- **Galais-Körper**
		- Gibt auch $\mathbb{F}_4\neq\mathbb{Z}_4$ (4 kein prim)
-
-
- **Grundbausteine der linearen Algebra**
	- **Tupel**
		- Menge $M$, $n\in\mathbb{Z}$
		- Abbildung $\overrightarrow{x}:\lbrace1,...,n\rbrace\rightarrow M$ ist ein n-Tupel mit der Einträgen aus der Menge M
			- $M^{n}:=M^{\lbrace1,...,n\rbrace}=Map(\lbrace1,...,n\rbrace,M)$
		- $\overrightarrow{x}:\lbrace1,...,n\rbrace\rightarrow M,k\mapsto x_{k}$ (**!!!** $\mapsto$ = Map)
		- $\overrightarrow{x}=(x_{k})_{k=1}^{n}=(x_1,...,x_{n})=$ {horizontales Tupel}
		- 2.2. Addition von Tupeln: $\overrightarrow{x}+\overrightarrow{y}:=(x_{k}+y_{k})_{k=1}^{n}$: => K ist eine abelsche Gruppe ($\overrightarrow{x}+\overrightarrow{y}=(x_{k}+y_{k})_{k=1}^{n}=(y_{k}+x_{k})_{k=1}^{n}=\overrightarrow{y}+\overrightarrow{x}$)
		- neutrales Element: $\overrightarrow{0}=(0,...,0)$
		- inverses Element: $-\overrightarrow{x}=(-x_0,...,-x_{n})$
		- Beispiel
			- $R^2$
			- (2/3)+(1/-1)=(3/2) => nummern über einander
		- *Multiplikation mit Skalaren*
			- K sei ein Körper, $n\in\mathbb{N}$
			- $K\times K^{n}\rightarrow K^{n},(\alpha,\overrightarrow{x})\mapsto\alpha\cdot\overrightarrow{x}:=(\alpha\cdot x_{k})_{k=1}^{n}$
		- 2.4. Rechnen mit Tupeln
			- Körper K, $n\in\mathbb{N}$
			- für alle $\overrightarrow{x},\overrightarrow{y}\in K^{n}$ und alle $\alpha,\beta\in K$
				- $\alpha(\overrightarrow{x}+\overrightarrow{y})=\alpha\overrightarrow{x}+\alpha\overrightarrow{y}$
				  logseq.order-list-type:: number
				- $(\alpha+\beta)\overrightarrow{x}=\alpha\overrightarrow{x}+\beta\overrightarrow{x}$
				  logseq.order-list-type:: number
				- $(\alpha\beta)\overrightarrow{x}=\alpha(\beta\overrightarrow{x})$
				  logseq.order-list-type:: number
				- $1\cdot\overrightarrow{x}=\overrightarrow{x}$
				  logseq.order-list-type:: number
	- **Matrizen**