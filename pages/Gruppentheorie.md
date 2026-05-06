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
- # Gruppe
	- sei $\left(G,\circ\right)$ ein Monoid
	- $\left(G,\circ\right)$ ist eine Gruppe, wenn zusätzlich gilt
		- logseq.order-list-type:: number