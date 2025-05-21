alias:: Ring

-
- $(R,+,\cdot)$ Menge und zwei Verknüpfungen
-
- Es ist ein Ring, wenn
	- das Magma $(R,+)$ ist eine abelsche Gruppe, e wird mit 0 bezeichnet
	- das Distributivgesetz gilt ($a,b,c\in R:a\cdot(b+c)=ab+ac$)
	- das Magma $(R,\cdot)$ ist eine Halbgruppe
-
- **besondere Ringe**
	- *kommutativer Ring*: $(R,\cdot)$ ist kommutativ
	- *unitärer Ring*: $(R,\cdot)$ ist ein Monoid, e wird als 1 bezeichnet (die eins des Rings)
		- $R^{\times}\coloneqq \lbrace r\in R:\exists e^{-1}\in R:r\cdot r^{-1}=1\rbrace$ ist die EInheitengruppe des untären Rings
		- Die Elemente von $R^{\times}$ heißen Einheiten
	- *Integritätsring*: R ist ein kommutativerm unitärer Ring mit der EIgenschaft $\forall x,y\in R\setminus\lbrace0\rbrace:xy\neq0$
		- R ist nullteilerfrei
		- Beispiel
			- $\mathbb{Z}$ mit der Einheitengruppe $R^{\times}=\lbrace1,-1\rbrace$
			- $x,y,z\in R:x\neq0$, dann $xy=xz\Rightarrow y=z$ (Kürzung)
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