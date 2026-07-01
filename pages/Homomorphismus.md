alias:: Gruppenhomomorphismus

- # Homomorphismus
	- ist eine Abbildung $\varphi:G\rightarrow H$, sodass gilt
		- logseq.order-list-type:: number
		  $$\varphi\left(e_{G}\right)=e_{H}$$
		- logseq.order-list-type:: number
		  $$\forall a,b\in G:\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
	- Homomorphieeigenschaft:
	  $$\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
	- $$\forall g\in G:\varphi\left(g^{-1}\right)=\varphi\left(g\right)^{-1}$$
- ## Ker und Img
	- Für einen Gruppenhomomorphismus $\varphi\left(G\right)\rightarrow H$ definieren wir
		- $$\ker\left(\varphi\right)\coloneqq\left\lbrace g\in G\mid\varphi\left(g\right)=e_{H}\right\rbrace\leq G$$
		- $$\text{Im}\left(\varphi\right)\coloneqq\left\lbrace h\in H\mid\exists g\in G:\varphi\left(g\right)=h\right\rbrace\subseteq H$$
- ## Gruppenhomomorphismus
  id:: 6a2031d9-2917-446e-8f19-38f54c75d99a
	- sind $G,H$ Gruppen, so erhalten wir analog einen **Gruppenhomomorphismus**
	  id:: 6a2031d9-597c-410d-bfbc-defdaf7bd8bb
- ## Isomorphismus
	- ist $\varphi$ zudem bijektiv (d.h. es existiert eine Abbildung $\varphi^{-1}:H\rightarrow G$ mit $\varphi\circ\varphi^{-1}=id_{H},\varphi^{-1}\circ\varphi=id_{G}$), dann heißt $\varphi$ ein Monoid- bzw. Gruppen- **isomophismus**
		- Kurznotation: $G\cong H$
- ## Monomorphismus
	- injektive (Gruppen-) Homomorphismen heißen Monomorphismus
- ## Epimorphismus
	- surjektive (Gruppen-) Homomorphismen heißen Epimorphismus
- ## Endomorphismus
	- $G,H:\left(G,\ast\right)=\left(H\cdot\right)$, so heißt ein (Gruppen-) Homomorphismus $\varphi$ ein **Endomorphismus**
- ## Automorphismus
	- ist $\varphi$ zudem ein Isomorphismus, so heißt $\varphi$ ein **Automorphismus**
	- wir bezeichnen alle Automorphismen auf $G$ als $\text{Aut}G$
		- $\text{Aut}G$ bildet mir Hintereinanderausführung $\circ$ eine Gruppe (Automorphiegruppe von $G$)
-
- [[Homomorphiesatz]]
-
- # Ringhomomorphismus
	- seien $\left(R,+,\cdot\right),\left(H,\oplus,\odot\right)$ Ringe mit $1_{R},1_{H}$
	- $\varphi:R\rightarrow H$ heißen Ringhomomorphismus, falls $\forall a,b\in R$ gilt
	  logseq.order-list-type:: number
		- logseq.order-list-type:: number
		  $$\varphi\left(a+b\right)=\varphi\left(a\right)\oplus\varphi\left(b\right)$$
		  (Gruppenhomomorphismus)
		- logseq.order-list-type:: number
		  $$\varphi\left(a\cdot b\right)=\varphi\left(a\right)\odot\varphi\left(b\right)$$
		  (Monoidhomomorphismus)
		- logseq.order-list-type:: number
		  $$\varphi\left(1_{R}\right)=1_{H}$$
	- Alle spezialisierten Bezeichnungen von Homomorphismen übertragen sich auf Ringhomomorphismen
	  logseq.order-list-type:: number
	- Sind $R$ und $H$ Körper, dann ist $\varphi$ ein Körperhomomorphismus
	  logseq.order-list-type:: number
- ## Eigenschaften
	- sei $\varphi:R\rightarrow R^{\prime}$ ein Ringhomomorphismus
	- $\ker\varphi$ ist ein Ideal in $R$
	  logseq.order-list-type:: number
	- $\text{im}\varphi$ ist ein Unterring von $R^{\prime}$ (nicht im Allgemeinen ein Ideal)
	  logseq.order-list-type:: number
	- Schränkt man $\varphi$ ein auf die Einheitengruppen $R^{\times}$ und $R^{\prime\times}$ von $R$ und $R^{\prime}$ , so wird dadurch ein Gruppenhomomorphismus bzgl. der Multiplikation induziert
	  logseq.order-list-type:: number
-