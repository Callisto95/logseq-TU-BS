## Homomorphismus
	- ist eine Abbildung $\varphi:G\rightarrow H$, sodass gilt
		- logseq.order-list-type:: number
		  $$\varphi\left(e_{G}\right)=e_{H}$$
		- logseq.order-list-type:: number
		  $$\forall a,b\in G:\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
	- Homomorphieeigenschaft:
	  $$\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
- ### Gruppenhomomorphismus
	- sind $G,H$ Gruppen, so erhalten wir analog einen **Gruppenhomomorphismus**
- ### Isomorphismus
	- ist $\varphi$ zudem bijektiv (d.h. es existiert eine Abbildung $\varphi^{-1}:H\rightarrow G$ mit $\varphi\circ\varphi^{-1}=id_{H},\varphi^{-1}\circ\varphi=id_{G}$), dann heißt $\varphi$ ein Monoid- bzw. Gruppen- **isomophismus**
		- Kurznotation: $G\cong H$
- ### Monomorphismus
	- injektive bzw. surjektive (Gruppen-) Homomorphismen heißen **Monomorphismus** (bzw. Epimorphismus)
- ### Endomorphismus
	- $G,H:\left(G,\ast\right)=\left(H\cdot\right)$, so heißt ein (Gruppen-) Homomorphismus $\varphi$ ein **Endomorphismus**
- ### Automorphismus
	- ist $\varphi$ zidem ein Isomorphismus, so heißt $\varphi$ ein **Automorphismus**
	- wir bezeichnen alle Automorphismen auf $G$ als $\text{Aut}G$
		- $\text{Aut}G$ bildet mir Hintereinanderausführung $\circ$ eine Gruppe (Automorphiegruppe von G)