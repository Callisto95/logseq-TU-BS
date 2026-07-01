# Homomorphiesatz (Ringe)
- ## ausführliche Variante
	- sei $\varphi:R\rightarrow R^{\prime}$ ein Ringhomomorphismus mit $I\subseteq R$ ein Ideal mit $I\subseteq\ker\varphi$
	- Dann existiert ein eindeutiger Ringhomomorphismus $\overline{\varphi}:R/I\rightarrow R^{\prime}$ mit $\varphi=\overline{\varphi}\circ\pi$
	- damit wird erzeugt
	  $$R\longrightarrow{}_{\varphi}R^{\prime};R\longrightarrow{}_{\pi}R/I\longrightarrow{}_{\overline{\varphi}}R^{\prime}$$
	- Außerdem gilt
		- $$\text{im}\varphi=\text{im}\overline{\varphi}$$
		- $$\ker\overline{\varphi}=\pi\ker\varphi$$
		- $$\ker\varphi=\pi^{-1}\ker\overline{\varphi}$$
		- wenn $I=\ker\varphi$ gilt, dann ist $\overline{\varphi}$ injektiv
- ## kurze Variante
	- sei $\varphi:R\rightarrow R^{\prime}$ ein Ringhomomorphismus
	- dann gilt
	  $$R/\ker\varphi\cong\text{im}\varphi\subseteq R$$
- ## Aussagen
	- sei $m\in\mathbb{N}$
	  $$m\in\mathbb{P}\Leftrightarrow\mathbb{Z}/m\mathbb{Z}\text{ ist ein Integritätsbereich}\Leftrightarrow\mathbb{Z}/m\mathbb{Z}\text{ ist ein Körper}$$
	- sei $p\in\mathbb{P}$. Der Körper $\mathbb{Z}_{p}=\mathbb{Z}/p\mathbb{Z}$ wird mit $\mathbb{F}_{p}$ bezeichnet