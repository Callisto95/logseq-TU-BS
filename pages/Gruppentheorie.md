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
- # Monoid
	- reference:: 4.1
	- Sei G eine Menge und $\circ:G\times G\rightarrow G$ eine Abbildung
	- $\left(G,\circ\right)$ ist ein Monoid, wenn
		- $\circ$ ist assoziativ:
		  logseq.order-list-type:: number
		  $$\forall a,b,c\in G:\left(a\circ b\right)\circ c=a\circ\left(b\circ c\right)$$
		- es existiert ein neutrales Element $e$:
		  logseq.order-list-type:: number
		  $$\forall g\in G:g\circ e=e\circ g=g$$
- id:: 69fb1229-ea15-4250-8620-b1c57134f6fe
- ### Untermonoid
	- sei $\left(G,\circ\right)$ ein Monoid und $H\subseteq G$ eine Teilmenge
	- Wenn $\left(H,\circ\right)$ eine Monoid ist, dann heißt $\left(H,\circ\right)$ ein Untermonoid von $G$
	- benötigt wird:
		- $e\in H$
		  logseq.order-list-type:: number
		- $\forall a,b\in H:a\circ b\in H$
		  logseq.order-list-type:: number
-
- # Gruppe
	- sei $\left(G,\circ\right)$ ein Monoid
	- $\left(G,\circ\right)$ ist eine Gruppe, wenn zusätzlich gilt
		- für alle $g\in G$ existiert ein *inverses Element* $g^{-1}\in G$
		  $$\forall g\in G:\exists g^{-1}\in G:g\circ g^{-1}=g^{-1}\circ g=e$$
-
- ### Untergruppen
	- sei $\left(G,\circ\right)$ eine Gruppe
	- falls zusätzlich zu den untermonoidischen Bedingungen gilt: $\forall a\in H:a^{-1}\in H$, dann ist $\left(H,\circ\right)$ eine Untergruppe von $G$
	- Notation: $H\leq G$
-
- ### Triviale Untergruppe
	- Jede Gruppe $\left(G,\circ\right)$ ist Untergruppe von sich selbst
	- $\left\lbrace e\right\rbrace$ ist triviale Untergruppe von $\left(G,\circ\right)$
	- Nichttriviale Untergruppen heißen *echte Untergruppen* (proper)
-
- ## Halbgruppe
	- ein Monoid ohne das neutrale Element
-
- ---
-
- # abelsche Strukturen
	- sei $\left(G,\circ\right)$ ein Monoid oder eine Gruppe
	- $\left(G,\circ\right)$ ist ein *abelsches Monoid* (bzw. *abelsche Gruppe*), wenn gilt
	  $$\forall g,h\in G:g\circ h=h\circ g$$
	- auch: "kommutatives Monoid" und "kommutative Gruppe"
-
- # Notationen
	- logseq.order-list-type:: number
	  $$a^{n}\coloneqq a\circ...\circ a\text{ (n-Mal)}$$
	- logseq.order-list-type:: number
	  $$a^{-n}\coloneqq\left(a^{-1}\right)^{n}$$
	- logseq.order-list-type:: number
	  $$\forall a,b\in G:ab=a\circ b$$
		- nur solange Verknüpfung klar ist
-
- ---
-
- $\left(\mathbb{Z}_{m}^{\ast},\cdot\right)$ ist auf jeden Fall eine Gruppe, wenn $m\in\mathbb{P}$ (durch [[kleiner Satz Fermat]])
-