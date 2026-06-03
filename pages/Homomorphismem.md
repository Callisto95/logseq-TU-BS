# Homomorphismus
	- ist eine Abbildung $\varphi:G\rightarrow H$, sodass gilt
		- logseq.order-list-type:: number
		  $$\varphi\left(e_{G}\right)=e_{H}$$
		- logseq.order-list-type:: number
		  $$\forall a,b\in G:\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
	- Homomorphieeigenschaft:
	  $$\varphi\left(a\cdot b\right)=\varphi\left(a\right)\cdot\varphi\left(b\right)$$
	  $$\forall g\in G:\varphi\left(g^{-1}\right)=\varphi\left(g\right)^{-1}$$
- ## Gruppenhomomorphismus
	- sind $G,H$ Gruppen, so erhalten wir analog einen **Gruppenhomomorphismus**
- ## Isomorphismus
	- ist $\varphi$ zudem bijektiv (d.h. es existiert eine Abbildung $\varphi^{-1}:H\rightarrow G$ mit $\varphi\circ\varphi^{-1}=id_{H},\varphi^{-1}\circ\varphi=id_{G}$), dann heißt $\varphi$ ein Monoid- bzw. Gruppen- **isomophismus**
		- Kurznotation: $G\cong H$
- ## Monomorphismus
	- injektive bzw. surjektive (Gruppen-) Homomorphismen heißen **Monomorphismus** (bzw. Epimorphismus)
- ## Endomorphismus
	- $G,H:\left(G,\ast\right)=\left(H\cdot\right)$, so heißt ein (Gruppen-) Homomorphismus $\varphi$ ein **Endomorphismus**
- ## Automorphismus
	- ist $\varphi$ zidem ein Isomorphismus, so heißt $\varphi$ ein **Automorphismus**
	- wir bezeichnen alle Automorphismen auf $G$ als $\text{Aut}G$
		- $\text{Aut}G$ bildet mir Hintereinanderausführung $\circ$ eine Gruppe (Automorphiegruppe von G)
-
- **kanonische Projektion**
	- $$\Pi:G\rightarrow G/N,a\mapsto aN$$
		- Beispiel: $\mathbb{Z}\rightarrow\mathbb{Z}_{m},a\mapsto\overline{a}\bmod m$
-
- # Homomorphiesatz
	- "fundamental homomorphism theorem"
	- seien $\left(G,\cdot\right),\left(G^{\prime},\tilde{\cdot}\right)$ Gruppen, $\varphi:G\rightarrow G^{\prime}$ Gruppenhomomorphismus, sei $N\trianglelefteq G$ Normalteiler mit $N\subseteq\text{ker}\varphi$
	- Dann existiert ein eindeutiger Gruppenhomomorphismus $\overline{\varphi}:G/N\rightarrow G^{\prime}$ mit $\varphi=\overline{\varphi}\cdot\Pi$
		- $$G\longrightarrow{}_{\varphi}G^{\prime}|G\longrightarrow{}_{\Pi}G/N\longrightarrow{}_{\overline{\varphi}}G^{\prime}$$
	- Es gilt außerdem 
	  $$\text{Im}\overline{\varphi}=\text{Im}\varphi,\space\space\space\text{ker}\overline{\varphi}=\Pi\left(\text{ker}\varphi\right),\space\space\space\text{ker}\varphi=\Pi^{-1}\left(\text{ker}\overline{\varphi}\right)$$
- ## kurzer Homomorphiesatz
	- sei $\varphi:G\rightarrow G$ ein Gruppenhomomorphismus
	- Dann gilt
	  $$G/\text{ker}\varphi\cong\text{Im}\varphi$$
	- $$\text{ker}\varphi\trianglelefteq G,\space\space\space\text{Im}\varphi\leq G^{\prime}$$
-