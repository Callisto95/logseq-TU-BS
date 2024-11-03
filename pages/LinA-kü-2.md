exclude-from-graph-view:: true

-
- reelle Tripel
  logseq.order-list-type:: number
	- sei $a=\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix},b=\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix},c=\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$ reelle Tripel
	- assoziativ:
		- $a\times(b\times c)=(a\times b)\times c$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times(\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix})=(\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix})\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_2c_3-b_3c_2\\ b_3c_1-b_1c_3\\ b_1c_2-b_2c_1\end{pmatrix}=\begin{pmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_2b_1c_2-a_2b_2c_1-a_2b_3c_1+a_3b_1c_3\\ a_3b_2c_3-a_3b_3c_2-a_3b_1c_2+a_3b_2c_1\\ a_1b_2c_3-a_1b_3c_2-a_2b_2c_3+a_2c_3b_2\end{pmatrix}=\begin{pmatrix}a_3b_1c_3-a_1b_3c_3-a_1b_2c_2+a_2b_1c_2\\ a_1b_2c_1-a_2b_1c_1-a_2b_3c_3+a_3b_2c_3\\ a_2b_3c_2-a_3b_2c_2-a_3b_1c_1+a_1c_3b_1\end{pmatrix}$
		- Gleichungen sind nicht Äquivalent
		- Verknüpfung ist nicht assoziativ => keine Halbgruppe
			- Verknüpfung kann kein Monoid oder abelsche Gruppe werden
- Körper aus Matrizen
  logseq.order-list-type:: number
	- Körper:
		- $(K,+)$ ist eine abelsche Gruppe (neutrales Element: $\underline{0}:=\begin{pmatrix}0 & 0\\ 0 & 0\end{pmatrix}$)
		- Distributivgesetz gilt
		- $(K,\cdot)$ ist ein Monoid (neurales Element $\underline{1}:=\begin{pmatrix}1 & 0\\ 0 & 1\end{pmatrix}$)
	- Nutzung von $(\mathbb{R}^{2\times2},+)$ als kommutative Gruppe
	- Nutzung von $(\mathbb{R}^{2\times2},\cdot)$ als kommutative Halbgruppe
	- Beweise
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}+\underline{0}=\underline{x}\Rightarrow\begin{pmatrix}x & -y_{}\\ y & x\end{pmatrix}+\begin{pmatrix}0 & 0\\ 0 & 0\end{pmatrix}=\begin{pmatrix}x+0 & -y+0\\ y+0 & x+0\end{pmatrix}=\begin{pmatrix}x & -y\\ y & x\end{pmatrix}=\underline{x}$
		- $\underline{x}\in\mathbb{R}^{2\times2}:\underline{x}\cdot\underline{1}=\underline{x}\Rightarrow\begin{pmatrix}x & -y\\ y & x\end{pmatrix}\cdot\begin{pmatrix}1 & 0\\ 0 & 1\end{pmatrix}=\begin{pmatrix}1x+0y & 0x+1(-y)\\ 1y+0x & 0(-1)+1x\end{pmatrix}=\begin{pmatrix}x & -y\\ y & x\end{pmatrix}=\underline{x}$
		- $\underline{a},\underline{b},\underline{c}\in\mathbb{R}^{2\times2}:\underline{a}\cdot(\underline{b}+\underline{c})=\underline{ab}+\underline{ac}$
		- $\underline{a}=\begin{pmatrix}2 & 3\\ 4 & 5\end{pmatrix},\underline{b}=\begin{pmatrix}6 & 7\\ 8 & 9\end{pmatrix},\underline{c}=\begin{pmatrix}10 & 11\\ 12 & 13\end{pmatrix}$
		- $\underline{a}\cdot(\underline{b}+\underline{c})$
			- $\underline{a}\cdot\begin{pmatrix}16 & 18\\ 20 & 22\end{pmatrix}$
			- $\begin{pmatrix}32+60 & 36+66\\ 64+90 & 72+110\end{pmatrix}=\begin{pmatrix}92 & 112\\ 154 & 182\end{pmatrix}$
		- $\underline{ab}+\underline{ac}$
			- $\begin{pmatrix}12+16 & 14+27\\ 24+40 & 21+45\end{pmatrix}+\begin{pmatrix}20+36 & 22+39\\ 40+60 & 44+\end{pmatrix}$