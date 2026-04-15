exclude-from-graph-view:: true

-
- reelle Tripel
  logseq.order-list-type:: number
  collapsed:: true
	- sei $a=\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix},b=\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix},c=\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$ reelle Tripel
	- assoziativ:
		- $a\times(b\times c)=(a\times b)\times c$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times(\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix})=(\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix})\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_2c_3-b_3c_2\\ b_3c_1-b_1c_3\\ b_1c_2-b_2c_1\end{pmatrix}=\begin{pmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_2b_1c_2-a_2b_2c_1-a_2b_3c_1+a_3b_1c_3\\ a_3b_2c_3-a_3b_3c_2-a_3b_1c_2+a_3b_2c_1\\ a_1b_2c_3-a_1b_3c_2-a_2b_2c_3+a_2c_3b_2\end{pmatrix}=\begin{pmatrix}a_3b_1c_3-a_1b_3c_3-a_1b_2c_2+a_2b_1c_2\\ a_1b_2c_1-a_2b_1c_1-a_2b_3c_3+a_3b_2c_3\\ a_2b_3c_2-a_3b_2c_2-a_3b_1c_1+a_1c_3b_1\end{pmatrix}$
		- Gleichungen sind nicht Äquivalent
		- Verknüpfung ist nicht assoziativ => keine Halbgruppe
			- Verknüpfung kann kein Monoid oder abelsche Gruppe werden
	- neutrales Element
		- $\exists e:\forall a\in\mathbb{R}^3:a\times e=a$
		- aber $e\times e\neq e$, denn $e\times e$ muss e sein
			- e muss $\overrightarrow{0}$ sein, aber $\overrightarrow{x}\times\overrightarrow{0}\neq\overrightarrow{x}$
	- inverses Element durch nichtexistenz des neutrales Element existiert auch nicht
	- kommutativ
		- $\forall\overrightarrow{a},\overrightarrow{b}\in\mathbb{R}^3:a\times b=b\times a$
		- $\begin{pmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{pmatrix}\neq\begin{pmatrix}a_3b_2-a_2b_3\\ a_1b_3-a_3b_1\\ a_2b_1-a_1b_2\end{pmatrix}$
- Körper aus Matrizen
  logseq.order-list-type:: number
  collapsed:: true
	- Körper:
		- $(K,+)$ ist eine abelsche Gruppe (neutrales Element: $e=\underline{0}\coloneqq \begin{bmatrix}0 & 0\\ 0 & 0\end{bmatrix}$)
		- Distributivgesetz gilt
		- $(K,\cdot)$ ist ein Monoid (neurales Element $e=\underline{1}\coloneqq \begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}$)
	- Nutzung von $(\mathbb{R}^{2\times2},+)$ als kommutative Gruppe
	- Nutzung von $(\mathbb{R}^{2\times2},\cdot)$ als kommutative Halbgruppe
	-
	- Beweise
		- $(K,+)\subseteq(\mathbb{R^{2\times2}},+)$
		-
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}+\underline{0}=\underline{x}\Rightarrow\begin{bmatrix}x & -y\\ y & x\end{bmatrix}+\begin{bmatrix}0 & 0\\ 0 & 0\end{bmatrix}=\begin{bmatrix}x+0 & -y+0\\ y+0 & x+0\end{bmatrix}=\begin{bmatrix}x & -y\\ y & x\end{bmatrix}=\underline{x}$
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}\cdot\underline{1}=\underline{x}\Rightarrow\begin{bmatrix}x & -y\\ y & x\end{bmatrix}\cdot\begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}=\begin{bmatrix}1x+0y & 0x+1(-y)\\ 1y+0x & 0(-1)+1x\end{bmatrix}=\begin{bmatrix}x & -y\\ y & x\end{bmatrix}=\underline{x}$
		- $\underline{a},\underline{b},\underline{c}\in\mathbb{R}^{2\times2}:\underline{a}\cdot(\underline{b}+\underline{c})=\underline{ab}+\underline{ac}$
		- $\underline{a}=\underline{0},\underline{b}=\underline{1},\underline{c}=\begin{bmatrix}x & -y\\ y & x\end{bmatrix}$
		- $\underline{a}\cdot(\underline{b}+\underline{c})$
			- $\underline{1}\cdot\underline{c}=\underline{c}$
		- $\underline{ab}+\underline{ac}$
			- $\underline{0}+\underline{1}\cdot\underline{c}=\underline{c}$
- Rechnen mit Matrizen
  logseq.order-list-type:: number
	- Matrixgrößen
	  logseq.order-list-type:: number
		- $K^{m\times n}(K^{n\times o}\cdot K^{o\times p})=K^{m\times n}\cdot K^{n\times p}=K^{m\times p}$
		- $(K^{m\times n}\cdot K^{n\times o})K^{o\times p}=K^{m\times o}\cdot K^{o\times p}=K^{m\times p}$
		-
		- $(a\cdot b)\cdot c$
		- $[\sum_{l=1}^{n}a_{kl}b_{lj}]_{k=1,j=1}^{m,o}\cdot c$
		- $[\sum_{i=1}^{o}\sum_{l=1}^{n}a_{kl}b_{lj}c_{ji}]_{k=1,j=1}^{m,p}$
		- selbes passiert auch bei $a\cdot(b\cdot c)$
	- Transposition
	  logseq.order-list-type:: number
		- $[a_{jk}]_{j=1,k=1}^{m,n}\cdot[b_{kl}]_{k=1,l=1}^{n,o}=[\sum_{l=1}^{n}a_{kl}b_{lj}]_{k=1,j=1}^{m,o}$
		- -> Transposition: $[\sum_{l=1}^{n}a_{kl}b_{lj}]_{k=1,j=1}^{m,o}$
		-
		- Transposition: $[a_{lk}]_{k=1,l=1}^{m,n}\cdot[b_{jl}]_{l=1,j=1}^{n,o}$
		- -> $[\sum_{l=1}^{n}a_{kl}b_{lj}]_{k=1,j=1}^{m,o}$
	- Berechnen
	  logseq.order-list-type:: number
		- nicht kommutativ