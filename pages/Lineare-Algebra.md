- Grundlagen:
	- [[Zahlenbereiche]]
	- [[Mengen-mit-Verknüpfung]]
	- [[Äquivalenzrelation]]
	-
	- **Potenzmenge**: 2^{M}$: Menge aller Teilmengen
	- **Kardinalität**: $|M|$: Anzahl der Elemente in $M$
	-
	- Restklassen:
		- $n \in \mathbb{N}; n \mathbb{Z} := { n \ast j : j \in \mathbb{R} }$
		- $(k, l) \in mod(n) <=> k \sim l \thinspace mod(n) <=> n|(k-l) <=> (k-l) \in n \mathbb{Z}$
			- "|" = teilt -> "n teilt"
		- damit Äquivalenzrelation mod(n) auf $\mathbb{Z}$ definiert
		- $k \sim l \thinspace mod(n)$: k und l haben bei Division durch n denselben Rest ($25\sim15 \ mod(10)$)
	- Äquivalenzklassen:
		- $[k]_n = \{l \in \mathbb{Z}: k \sim l \ mod(n)\} = \{l \in \mathbb{Z}: k - l \in \mathbb{Z}\} = k + n\mathbb{Z}$
			- disjunkte Zerlegung in Äquivalenzklassen
			- $\mathbb{Z}=\uplus_{k=0}^{n-1}[k]_{n}=[0]_{n}\biguplus[1]_{n}\biguplus...\biguplus[n-1]_{n}$
			- $^n[n]_n$
		- Menge der Restklassen
			- $\mathbb{Z}_n = \mathbb{Z}/n\mathbb{Z} := \{[k]_n: k \in \mathbb{R}\} = \{[0]_n, ..., [n-1]_n\}$
				- mit k=0,...,n-1 unterschiedliche Restklassen
			- Rechenoperationen
				- Addition der Restklassen: $[k]_{n} \oplus [l]_{n}=[k+l]_{n}$
				- Multiplikation der Restklassen: $[k]_{n} \odot [l]_{n}=[k \ast l]_{n}$
			- Vereinfacht:
				- $\mathbb{Z} = \{0, ..., n-1\}$ repäsentiert die Abbildung für Klasse $[0]_n = n\mathbb{Z}$
				- Bsp: 1 + 1 = 0, aber $[1]_2 \oplus [1]_2 = [0]_2$ gemeint; 1 + 1 = 0, mod(2)
	- Einheitengruppe:
		- Monoid (M, *) mit neutralen Element $e \in M$
			- $M^x := \{g \in M: \exists \widetilde{g} \in M: g \ast \widetilde{g} = e\}$ Einheitengruppe von M
	- Rechnen mit Abbildungen:
		- Map (M,, M): Menge aller Abbildungen, f: M -> M
		- $\ast$ Verkettung von Abbildungen, $f,g \in Map(M, M), f \ast g$: M -g-> M -f-> M
			- nicht kommutativ
		- neutrales Element: identische Abbildung $I_M: I_M(x) = x; \forall x \in M$
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
- **Korollar**
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
		- bsp: a=1$-1+1=0=[\cdot-1]\Rightarrow(-1)^2+(-1)=0=[+1]\Rightarrow(-1)^2=1=1^2$
		  logseq.order-list-type:: number