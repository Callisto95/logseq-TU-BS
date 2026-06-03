- **kanonische Projektion**
	- $$\Pi:G\rightarrow G/N,a\mapsto aN$$
		- Beispiel: $\mathbb{Z}\rightarrow\mathbb{Z}_{m},a\mapsto\overline{a}\bmod m$
-
- # Homomorphiesatz
	- "fundamental homomorphism theorem"
	- seien $\left(G,\cdot\right),\left(G^{\prime},\tilde{\cdot}\right)$ Gruppen, $\varphi:G\rightarrow G^{\prime}$ Gruppenhomomorphismus, sei $N\trianglelefteq G$ Normalteiler mit $N\subseteq\ker\varphi$
	- Dann existiert ein eindeutiger Gruppenhomomorphismus $\overline{\varphi}:G/N\rightarrow G^{\prime}$ mit $\varphi=\overline{\varphi}\cdot\Pi$
		- $$G\longrightarrow{}_{\varphi}G^{\prime}|G\longrightarrow{}_{\Pi}G/N\longrightarrow{}_{\overline{\varphi}}G^{\prime}$$
	- Es gilt außerdem 
	  $$\text{Im}\overline{\varphi}=\text{Im}\varphi,\space\space\space\ker\overline{\varphi}=\Pi\left(\ker\varphi\right),\space\space\space\ker\varphi=\Pi^{-1}\left(\ker\overline{\varphi}\right)$$
- ## kurzer Homomorphiesatz
	- sei $\varphi:G\rightarrow G$ ein Gruppenhomomorphismus
	- Dann gilt
	  $$G/\ker\varphi\cong\text{Im}\varphi$$
	- $$\ker\varphi\trianglelefteq G,\space\space\space\text{Im}\varphi\leq G^{\prime}$$
	- ---
	- $$\dim V=\dim\ker\varphi+\dim\text{Im}\varphi$$
-