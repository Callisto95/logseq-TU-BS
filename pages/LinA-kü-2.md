exclude-from-graph-view:: true

-
- reelle Tripel
  logseq.order-list-type:: number
  collapsed:: true
	- sei $a=\begin{bmatrix}a_1\\ a_2\\ a_3\end{bmatrix},b=\begin{bmatrix}b_1\\ b_2\\ b_3\end{bmatrix},c=\begin{bmatrix}c_1\\ c_2\\ c_3\end{bmatrix}$ reelle Tripel
	- assoziativ:
		- $a\times(b\times c)=(a\times b)\times c$
		- $\begin{bmatrix}a_1\\ a_2\\ a_3\end{bmatrix}\times(\begin{bmatrix}b_1\\ b_2\\ b_3\end{bmatrix}\times\begin{bmatrix}c_1\\ c_2\\ c_3\end{bmatrix})=(\begin{bmatrix}a_1\\ a_2\\ a_3\end{bmatrix}\times\begin{bmatrix}b_1\\ b_2\\ b_3\end{bmatrix})\times\begin{bmatrix}c_1\\ c_2\\ c_3\end{bmatrix}$
		- $\begin{bmatrix}a_1\\ a_2\\ a_3\end{bmatrix}\times\begin{bmatrix}b_2c_3-b_3c_2\\ b_3c_1-b_1c_3\\ b_1c_2-b_2c_1\end{bmatrix}=\begin{bmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{bmatrix}\times\begin{bmatrix}c_1\\ c_2\\ c_3\end{bmatrix}$
		- $\begin{bmatrix}a_2b_1c_2-a_2b_2c_1-a_2b_3c_1+a_3b_1c_3\\ a_3b_2c_3-a_3b_3c_2-a_3b_1c_2+a_3b_2c_1\\ a_1b_2c_3-a_1b_3c_2-a_2b_2c_3+a_2c_3b_2\end{bmatrix}=\begin{bmatrix}a_3b_1c_3-a_1b_3c_3-a_1b_2c_2+a_2b_1c_2\\ a_1b_2c_1-a_2b_1c_1-a_2b_3c_3+a_3b_2c_3\\ a_2b_3c_2-a_3b_2c_2-a_3b_1c_1+a_1c_3b_1\end{bmatrix}$
		- Gleichungen sind nicht Äquivalent
		- Verknüpfung ist nicht assoziativ => keine Halbgruppe
			- Verknüpfung kann kein Monoid oder abelsche Gruppe werden
	- neutrales Element
		- $\exists e:\forall a\in\mathbb{R}^3:a\times e=a$
		- aber $e\times e\neq e$, denn $e\times e=e$
			- e muss $\overrightarrow{0}$ sein, aber $\overrightarrow{x}\times\overrightarrow{0}\neq\overrightarrow{x}$
	- inverses Element durch nichtexistenz des neutrales Element existiert auch nicht (?)
	- kommutativ
		- $\forall\overrightarrow{a},\overrightarrow{b}\in\mathbb{R}^3:a\times b=b\times a$
		- $\begin{bmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{bmatrix}\neq\begin{bmatrix}a_3b_2-a_2b_3\\ a_1b_3-a_3b_1\\ a_2b_1-a_1b_2\end{bmatrix}$
- Körper aus Matrizen
  logseq.order-list-type:: number
	- Körper:
		- $(\mathbb{R}^{2\times2},+)$ ist eine abelsche Gruppe (neutrales Element: $e=\underline{0}:=\begin{bmatrix}0 & 0\\ 0 & 0\end{bmatrix}$)
		- Distributivgesetz gilt
		- $(\mathbb{R}^{2\times2},\cdot)$ ist ein Monoid (neurales Element $e=\underline{1}:=\begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}$)
	- Nutzung von $(\mathbb{R}^{2\times2},+)$ als kommutative Gruppe
	- Nutzung von $(\mathbb{R}^{2\times2},\cdot)$ als kommutative Halbgruppe
	- Beweise
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}+\underline{0}=\underline{x}\Rightarrow\begin{bmatrix}x & -y_{}\\ y & x\end{bmatrix}+\begin{bmatrix}0 & 0\\ 0 & 0\end{bmatrix}=\begin{bmatrix}x+0 & -y+0\\ y+0 & x+0\end{bmatrix}=\begin{bmatrix}x & -y\\ y & x\end{bmatrix}=\underline{x}$
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}\cdot\underline{1}=\underline{x}\Rightarrow\begin{bmatrix}x & -y\\ y & x\end{bmatrix}\cdot\begin{bmatrix}1 & 0\\ 0 & 1\end{bmatrix}=\begin{bmatrix}1x+0y & 0x+1(-y)\\ 1y+0x & 0(-1)+1x\end{bmatrix}=\begin{bmatrix}x & -y\\ y & x\end{bmatrix}=\underline{x}$
		- $\underline{a},\underline{b},\underline{c}\in\mathbb{R}^{2\times2}:\underline{a}\cdot(\underline{b}+\underline{c})=\underline{ab}+\underline{ac}$
		- $\underline{a}=\begin{bmatrix}2 & 3\\ 4 & 5\end{bmatrix},\underline{b}=\begin{bmatrix}6 & 7\\ 8 & 9\end{bmatrix},\underline{c}=\begin{bmatrix}10 & 11\\ 12 & 13\end{bmatrix}$
		- $\underline{a}\cdot(\underline{b}+\underline{c})$
			- $\begin{bmatrix}2 & 3\\ 4 & 5\end{bmatrix}\cdot\begin{bmatrix}16 & 18\\ 20 & 22\end{bmatrix}$
			- $\begin{bmatrix}32+60 & 36+66\\ 64+100 & 72+110\end{bmatrix}=\begin{bmatrix}92 & 102\\ 164 & 182\end{bmatrix}$
		- $\underline{ab}+\underline{ac}$
			- $\begin{bmatrix}12+24 & 14+27\\ 24+40 & 28+45\end{bmatrix}+\begin{bmatrix}20+36 & 22+39\\ 40+60 & 44+65\end{bmatrix}=\begin{bmatrix}36 & 41\\ 64 & 73\end{bmatrix}+\begin{bmatrix}56 & 61\\ 100 & 109\end{bmatrix}=\begin{bmatrix}92 & 102\\ 164 & 182\end{bmatrix}$
- Rechnen mit Matrizen
  logseq.order-list-type:: number
	-