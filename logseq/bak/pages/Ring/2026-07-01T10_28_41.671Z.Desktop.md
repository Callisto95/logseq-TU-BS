# Defintion
- sei $(R,+,\cdot)$ Menge und zwei Verknüpfungen
- $(R,+,\cdot)$ ist ein Ring, wenn
	- $(R,+)$ ist eine abelsche Gruppe
		- $e$ wird mit 0 bezeichnet
	- $(R,\cdot)$ ist ein Monoid
		- $e$ wird mit 1 bezeichnet
	- das Distributivgesetz gilt
		- $$a,b,c\in R:a\cdot(b+c)=ab+ac$$
-
- # besondere Ringe
- ## kommutativer Ring
	- $(R\setminus\left\lbrace0\right\rbrace,\cdot)$ ist kommutativ
- ## unitärer Ring
	- $(R,\cdot)$ ist ein Monoid, $e$ wird als $\mathbb{1}$ bezeichnet (die eins des Rings)
- ## Integritätsring
	- $R$ ist ein kommutativerm unitärer Ring mit der EIgenschaft $\forall x,y\in R\setminus\lbrace0\rbrace:xy\neq0$
	- "$R$ ist nullteilerfrei"
	- Beispiel
	  collapsed:: true
		- $\mathbb{Z}$ mit der Einheitengruppe $R^{\times}=\lbrace1,-1\rbrace$
		- $x,y,z\in R:x\neq0$, dann $xy=xz\Rightarrow y=z$ (Kürzung)
- ## Körper
	- $\left(R,+,\cdot\right)$ ist ein komutativer Ring
	- $\left(R\setminus\left\lbrace0\right\rbrace,\cdot\right)$ ist eine Gruppe
- ## Unterring
	- seien $\left(R,+,\cdot\right),\left(S,+,\cdot\right)$ (mit denselben $+$ und $\cdot$)
	- Wenn $S\subseteq R$, dann ist $S$ ein Unterrung von $R$
- ## Nullring
	- $R=\left\lbrace0\right\rbrace$
	- dabie ist die 0 und die 1 das gleiche Element
-
- # Einheit
	- ein Element $r\in R$ heißt Einheit, wenn gilt
	  $$\exists r^{-1}\in R:r\cdot r^{-1}=1$$
	- $R^{\times}$ ist die Menge aller Einheiten in $R$
-
- Konstruktion der rationalen Zahlen
  collapsed:: true
	- $M\coloneqq \lbrace(x,y)\in\mathbb{Z^2}:y\neq0\rbrace$ seien durch die Relation $(x,y)\sim(u,v):\Leftrightarrow xv\sim uy$
	- Zeige, dass $\sim$ eine Äquivalenzrelation ist
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
			-
			- $(\ast\ast)$ $xv\cdot ut=uy\cdot sv$
				- Fall: $u=0$: aus $(\ast)$ ergibt sich $x=0$ und $s=0$, da v und y nicht 0 sein können (da sie der Nenner sind -> Äquivalenzrelation [Umformung zu Brüchen])
					- Dann ist $xt=0=sy$
				- Fall: $u\neq0$: Nullteilerfreiheit fordert $uv\neq0$
					- $(\ast\ast)$ $uvxt=uvsy$ =[$uv$ kürzen]=> $xt=sy$
			- ==> ist eine Äquivalenzrelation
-
- Addition rationaler Zahlen
  collapsed:: true
	- $M,\sim$ wie bei der Konstruktion rationaler Zahlen
	- $\mathbb{Q}\coloneqq M/\sim=\lbrace[x,y];x,y\in M\rbrace$ ist die Menge der Äquivalenzklassen bezüglich der Relation
	- Untersuche, durch welche Folgende Ansätze eine Verknüpfung auf den rationalen Zahlen $\mathbb{Q}$ definiert wird
		- a: $[(x,y)]\oplus[(u,v)]\coloneqq [(x+u),(y+v)]$ == $\frac{x}{y}\oplus\frac{u}{v}\coloneqq \frac{x+u}{y+v}$ => nicht Wahr (so werden nicht Brüche addiert)
			- $\frac12+\frac23=[(1,2)]\oplus[(2,3)]=[(1+2,2+3)]=[(3,5)]$
			  id:: 6716311d-ac39-4f59-a11a-32268d5bcfcd
			- $\frac24+\frac69=[(2,4)]\oplus[(6,9)]=[(2+6,4+9)]=[(8,13)]$
				- $[(3,5)]\neq[(8,13)]$
		- b: $[(x,y)]\#[(u,v)]\coloneqq [(xv+uy,yv)]$
			- $(x,y)=\frac{x}{y}$
			- $\frac{x}{y}\#\frac{u}{v}\coloneqq \frac{xv+uy}{yv}$
				- $\frac{x}{y}+\frac{u}{v}==\frac{xv+uy}{yv}$ repräsentatenunabhängig; $yv\neq0$ -> Nullteilerfreier Ring
			- $[(x,y)]=[(x^{\prime},y^{\prime})]$, sodass $xy^{\prime}=x^{\prime}y$ und $[(u,v)]=[(u^{\prime},v^{\prime})]$, sodass $uv^{\prime}=u^{\prime}v$
			- $(x,y)=[\frac{x}{y}]=\lbrace(u,v);(u,v)\sim(x,y)\rbrace==\frac{x}{y}=\frac{u}{v}==xv=uy==\frac{x}{y}\cdot\frac{u}{v}==\frac{xu}{yu}$
			- zeige, dass $[(x,y)]\#[(u,v)]=[(x^{\prime},y^{\prime})]\#[(u^{\prime},v^{\prime})]$
				- $(xv+uy,yv)\sim(x^{\prime}v^{\prime}+u^{\prime}y^{\prime},y^{\prime}v^{\prime})$
				- $xvy^{\prime}v^{\prime}+uyy^{\prime}v^{\prime}=x^{\prime}v^{\prime}yv+u^{\prime}y^{\prime}yv$
				- $(\ast)$ $xy^{\prime}vv^{\prime}=x^{\prime}yvv^{\prime}$ => einsetzen in ^, wodurch die Gleichung erfüllt ist
			- ===> # ist eine Verknüpfung auf $\mathbb{Q}$
-
- # Ideale
	- sei $\left(R,+,\cdot\right)$ ein Ring
	- Dann ist $I\subseteq R$ ein Ideal, wenn gilt
		- $$\left(I,+\right)\leq\left(R,+\right)$$
		- collapsed:: true
		  $$\forall a\in I,r\in R:r\cdot a\in I$$
			- eventuell auch
			  $$\forall a\in I,r\in R:r\cdot a=a\cdot r\in I$$
	- Wenn $I\neq R$, dann ist $I$ ein echtes Ideal
	- Beispiel
	  collapsed:: true
		- $\left(\text{Mat}\left(2\times2\right),+,\cdot\right)$ ist ein Ring
		- sei $D=\left\lbrace M\in\text{Mat}\left(2\times2\right)\middle|\text{det}\left(M)=0\right.\right\rbrace$
		- $$\begin{bmatrix}1 & 0\\ 0 & 0\end{bmatrix}+\begin{bmatrix}0 & 0\\ 0 & 1\end{bmatrix}=\begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}=I$$
		- => $D$ ist keine Gruppe bezüglich $+$
		- ---
		- sei $\left(R,+,\cdot\right)$ Ring, $I\subseteq R$ Ideal, $a\in I$ Einheit
		- => $I=R$, da
		- $$a\in I\Rightarrow\left\lbrack a^{-1}\right\rbrack_{\in R}\cdot\left\lbrack a\right\rbrack_{\in I}\in I\Rightarrow1\in I\Rightarrow I=R$$
		- => Ist $R$ ein Körper, dann ist jedes Ideal trivial
- ## Rechenregeln
	- sei $\left(R,+,\cdot\right)$ Ring, $I,J$ Ideale von $R$
	- folgende Mengen sind Ideale
		- logseq.order-list-type:: number
		  $$I\cap J$$
		- logseq.order-list-type:: number
		  $$I+J=\left\lbrace i+j\middle|i\in I,j\in J\right\rbrace$$
		- logseq.order-list-type:: number
		  $$I\cdot J=\left\lbrace\sum_{\text{endlich}}i\cdot j\middle|i\in I,j\in J\right\rbrace$$
- ## erzeugtes Ideal
	- sei $\left(R,+,\cdot\right)$ Ring, $I$ Ideal, $p_1,...,p_{s}\in I$
	- logseq.order-list-type:: number
	  $$\left\langle p_1,...,p_{s}\right\rangle=\left\lbrace\sum_{i=1}^{s}r_{i}\cdot p_{i}\middle|\forall i\in\left\lbrack s\right\rbrack:r_{i}\in R\right\rbrace$$
	  ist das von $p_1,...,p_2$ erzeugt Ideal über $R$
	- Wenn $I=\left\langle p_1,...,p_{s}\right\rangle$, dann heißen $p_1,...,p_{s}$ ein **Erzeugendensystem** von $I$
	  logseq.order-list-type:: number
	- Ideal $I$ heißt **endlich erzeugt**, falls es ein endliches Erzeugendensystem hat
	  logseq.order-list-type:: number
	- Wenn
	  logseq.order-list-type:: number
	  $$\exists p\in R:\left\langle p\right\rangle=I$$
	  dann heißt $I$ **Hauptideal**
	- ist $\left(R,+,\cdot\right)$ Integritätsbereich und jedes Ideal in $R$ ist ein Hauptideal, dann heißt $R$ **Hauptidealring**
- ### Hauptidealring der ganzen Zahlen
	- $\left(\mathbb{Z},+,\cdot\right)$ ist ein Hauptidealring
	- Beweis
		- $\mathbb{Z}$ ist ein Integritätsbereich, da Nullteilerfrei
			- $a\cdot b=0\Rightarrow a=0\lor b=0$
		- sei $I\subseteq\mathbb{Z}$ Ideal
		- Dann ist $\left(I,+\right)\leq\left(\mathbb{Z},-\right)$
		- Dann gilt nach Lemma 4.20 $I=m\mathbb{Z}$ für ein $m\in\mathbb{Z}$: $\Rightarrow I=\left\langle m\right\rangle$
		- => $I$ ist ein Hauptideal
		- durch Wiederholung mit allen $m$: $\mathbb{Z}$ ist ein Hauptideal
- ### irgendwas mit Hauptidealen
	- in einem Hauptidealring $R$ stimmen zwei Hauptideale $\left\langle p_1\right\rangle,\left\langle p_2\right\rangle$ genau dann überein, wenn es eine Einheit $q\in R$ gibt, sodass gilt
	  $$p_1=q\cdot p_2$$
	- Die Elemente $p_1,p_2$ heißen *assoziiert*
- ### Beispiele
	- $\left\langle2,x\right\rangle$ in $\mathbb{Z}\left\lbrack x\right\rbrack$ ist kein Hauptideal
	- $$\left\langle x\right\rangle=\left\lbrace\sum_{\text{endlich}}c_{i}x^{i}\middle|c_0=0\right\rbrace$$
	- $$\left\langle2\right\rangle=\left\lbrace\sum_{\text{endlich}}c_{i}x^{i}\middle|\forall i:2|c_{i}\right\rbrace$$
	- $$\left\langle2,x\right\rangle=\left\lbrace\sum_{\text{endlich}}c_{i}x^{i}\middle|2|c_0\right\rbrace$$
	- Die drei Ideale sind verschieden
	- Es gibt kein $p\left(x\right)$ in $\mathbb{Z}\left\lbrack x\right\rbrack$, das $x$ und $2$ als Vielfaches hat
	- $\left\langle x,2\right\rangle$ ist kein Hauptideal
	- $\mathbb{Z}\left\lbrack x\right\rbrack$ ist kein Hauptidealring
-