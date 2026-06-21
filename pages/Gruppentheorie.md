- random stuff aus Algebra
  collapsed:: true
	- ganze Zahlen $\mathbb{Z}$
	- reele, komplexe, rationale Zahlen $\mathbb{R},\mathbb{C}_{},\mathbb{Q}$
	- Matrizen $\text{Mat(n}\times n,\mathbb{R})$
	- Restklassen $\mathbb{Z}_{m}$
	- **=> Menge G von Objekten**
	- überall auf diesen Mengen
		- Addition
		- Multiplikation
		- (skalare Multiplikation)
		- modulare Arithmetik
		- **=> Operator $\circ:G\times G\rightarrow G$**
		- Beobachtung:
			- alle Operationen sind assoziativ
			- viele Operationen sind kommutativ
			- Operationen bestitzen ein neutrales Element
			- viele Mengen und Operationen liefern inverse Elemente zu gegebenen Elementen
-
- Regeln
	- $$e^{-1}=e$$
-
- # Monoid
	- reference:: 4.1
	- Sei $G$ eine Menge und $\circ:G\times G\rightarrow G$ eine Abbildung
	- $\left(G,\circ\right)$ ist ein Monoid, wenn
		- $\circ$ ist assoziativ:
		  logseq.order-list-type:: number
		  $$\forall a,b,c\in G:\left(a\circ b\right)\circ c=a\circ\left(b\circ c\right)$$
		- es existiert ein neutrales Element $e$:
		  logseq.order-list-type:: number
		  $$\forall g\in G:g\circ e=e\circ g=g$$
- ## Untermonoid
	- sei $\left(G,\circ\right)$ ein Monoid und $H\subseteq G$ eine Teilmenge
	- Wenn gilt:
		- $e\in H$
		  logseq.order-list-type:: number
		- $\forall a,b\in H:a\circ b\in H$
		  logseq.order-list-type:: number
	- dann ist $\left(H,\circ\right)$ ein Untermonoid von $G$
-
- # Gruppe
	- sei $\left(G,\circ\right)$ ein Monoid
	- $\left(G,\circ\right)$ ist eine Gruppe, wenn zusätzlich gilt
		- für alle $g\in G$ existiert ein *inverses Element* $g^{-1}\in G$
		  $$\forall g\in G:\exists g^{-1}\in G:g\circ g^{-1}=g^{-1}\circ g=e$$
- ## Halbgruppe
	- ein Monoid ohne das neutrale Element
- ## Untergruppe
	- sei $\left(G,\circ\right)$ eine Gruppe
	- falls zusätzlich zu den untermonoidischen Bedingungen gilt: $\forall a\in H:a^{-1}\in H$, dann ist $\left(H,\circ\right)$ eine Untergruppe von $G$
	- Notation: $H\leq G$
- ### Triviale Untergruppe
	- Jede Gruppe $\left(G,\circ\right)$ ist Untergruppe von sich selbst
	- $\left\lbrace e\right\rbrace$ ist triviale Untergruppe von $\left(G,\circ\right)$
	- Nichttriviale Untergruppen heißen *echte Untergruppen* (proper)
- [[zyklische Gruppe]]
- ### Normalteiler
	- reference:: 4.12
	- Eine Untergruppe $H\leq G$ heißt Normalteiler (normale Untergruppe) von $G$, falls
	  $$\forall a\in G:aH=Ha$$
		- kurz $H\trianglelefteq G$
	- ---
	- sei $\varphi:G\rightarrow G$ [Gruppenhomomorphismus]([[Homomorphismem]])
	- Dann ist $\ker\varphi$ Normalteiler in $G$
	- ---
	- Jede Untergruppe mit genau 2 Links- oder Rechtsnebenklassen ist ein Normalteiler
	- Beweis
	  collapsed:: true
		- sei $H\leq G,I=G\setminus H$
		- $\forall g\in G$:
		- Wenn $g\in H\Rightarrow gH=H=Hg$
		- Wenn $g\notin H:gH=I=Hg$
		- => Aufteilung von $G$ in $H$ und $I$
- ### Faktorgruppe
	- seien $\left(G,\cdot\right)$ Gruppe und $N\trianglelefteq G$ Normalteiler in $G$
	- Dann definieren wir eine Verknüpfung $\ast$ auf $G/N$ durch
	  $$\forall a,b\in G:\left(aN\right)\ast\left(bN\right)\coloneqq\left(a\cdot b\right)N$$
	- Wir nennen $\left(G/N,\ast\right)$ die Faktorgruppe von $G$ und $N$
-
- ---
-
- # abelsche Strukturen
	- sei $\left(G,\circ\right)$ ein Monoid oder eine Gruppe
	- $\left(G,\circ\right)$ ist ein abelsches Monoid (bzw. abelsche Gruppe), wenn gilt
	  $$\forall g,h\in G:g\circ h=h\circ g$$
	- auch: "kommutatives Monoid" bzw. "kommutative Gruppe"
-
- # Notationen
	- logseq.order-list-type:: number
	  $$a^{n}\coloneqq a\circ...\circ a\text{ (n-Mal)}$$
	- logseq.order-list-type:: number
	  $$a^{-n}\coloneqq\left(a^{-1}\right)^{n}$$
	- logseq.order-list-type:: number
	  $$\forall a,b\in G:ab=a\circ b$$
		- nur solange Verknüpfung klar ist!
-
- ---
-
- # Linkstranslation
	- sei $a\in G$ für eine Gruppe $\left(G,\cdot\right)$
	- Wir definieren die Linkstranslation $\tau_{a}\in\text{bij}\left(G\right)$ durch $\tau_{a}:G\rightarrow G,g\mapsto a\cdot g$
	- Dann ist die Abbildung $G\rightarrow\text{bij}\left(G\right),a\mapsto\tau_{a}$ ein injektiver Gruppenhomomorphismus
- # Linksnebenklasse
	- (left co-set)
	- sei $\left(G,\cdot\right)$ Gruppe und $H\subseteq G$ Untergruppe
	- Dann ist für ein $a\in G$ die Linksnebenklasse von $H$ in $G$ definiert als $a\cdot H\coloneqq\left\lbrace a\cdot h\mid h\in H\right\rbrace$
		- also $a\cdot H=\tau_{a}\left(H\right)$
	- bei $b\in H:b\cdot H=e\cdot H=H$
		- durch Abgeschlossenheit der Operation
	- Ein Element der Nebenklasse ist ein **Repräsentant** der Nebenklasse
		- Repräsentanten müssen wohldefiniert sein
	- Die Menge der Linksnebenklassen von $H$ in $G$ beichnen wir mit $G/H$
		- Die Kardinalität von $G/H$ nennen wir den **Index** von $G$ in $H$
			- kurz: $G:H$
	- $$\forall a\in G:a\in aH$$
	- $$\forall h\in H:hH=H$$
- ## Eigenschaften von Nebenklassen
	- reference:: 4.10
	- seien $G,H$ zwei Gruppen
	- Seien $aH$ und $bH$ Linksnebenklassen von $H$ in $G$ für $a,b\in G$.
	  logseq.order-list-type:: number
	  Dann sind folgendende Aussagen equivalent
	  $$aH=Ha\Leftrightarrow aH\cap bH\neq\varnothing\Leftrightarrow a\in bH\Leftrightarrow b^{-1}\cdot a\in H$$
	- Je zwei Linksnebenklassen von $H$ in $G$ sind identisch oder disjunkt und gleichmächtigt.
	  logseq.order-list-type:: number
	  $G$ ist die Vereinigung aller seiner Linksnebenklassen.
		- Beweis
			- Da die Linkstranslation $\tau_{a}:H\rightarrow aH$ eine Bijektion ist, sind $Ha$ und $aH$ *gleichmächtig*.
				- jede Nebenklasse ist gleich groß
			- Aus Teil 1. folgt, dass $aH$und $bH$ genau dann leeren Schnitt haben, falls sie nicht übereinstimmen.
			- Also sind verschiedene Linksnebenklassen disjunkt.
			- Da zudem für alle $a\in G$ gilt: $a\in aH$ folgt, dass $G$ disjunkte Vereinigungen seiner Linksnebenklassen ist.
-
- Sei $M$ eine Menge und $\sim$ eine Relation auf $M$.
	- Dann ist $\sim$ eine Äquivalenzrelation genau dann wenn sie reflexiv, symmetrisch, und transitiv ist.
	- Sei $a\in M$. Dann ist die Äquivalenzklasse gegeben durch $\left\lbrack a\right\rbrack_{\sim}=\left\lbrace b\in M\mid a\sim b\right\rbrace$
		- $$\forall a\in M:a\in\left\lbrack a\right\rbrack_{\sim}$$
-
- Theorem
	- $M$ ist die disjunkte Vereinigung seiner Äquivalenzklassen.
- Theorem
	- Ist $M_1,...,M_{n}$ disjunkte überdeckung von $M$ ist, dann definieren $M_1,...,M_{n}$ eine Äquivalenzrelation
-
- ## Korollar: Satz von Lagrange (Lagrange Theorem)
	- reference:: 4.11
	- Sei $G$ eine endliche Gruppe und $H\leq G$ eine Untergruppe
	- Dann gilt:
	  $$\text{ord}\left(G\right)=\text{ord}\left(H\right)\cdot\left(G:H\right)$$
-
- ---
-
- $\left(\mathbb{Z}_{m}^{\ast},\cdot\right)$ ist auf jeden Fall eine Gruppe, wenn $m\in\mathbb{P}$ (durch [[kleiner Satz Fermat]])
-