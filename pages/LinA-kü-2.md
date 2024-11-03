exclude-from-graph-view:: true

-
- reelle Tripel
  logseq.order-list-type:: number
	- sei $a=\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix},b=\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix},c=\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$ reelle Tripel
	- assoziativ:
		- $a\times(b\times c)=(a\times b)\times c$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times(\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix})=(\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_1\\ b_2\\ b_3\end{pmatrix})\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_1\\ a_2\\ a_3\end{pmatrix}\times\begin{pmatrix}b_2c_3-b_3c_2\\ b_3c_1-b_1c_3\\ b_1c_2-b_2c_1\end{pmatrix}=\begin{pmatrix}a_2b_3-a_3b_2\\ a_3b_1-a_1b_3\\ a_1b_2-a_2b_1\end{pmatrix}\times\begin{pmatrix}c_1\\ c_2\\ c_3\end{pmatrix}$
		- $\begin{pmatrix}a_2b_1c_2-a_2b_2c_1-a_2b_3c_1+a_3b_1c_3\\ a_3b_2c_3-a_3b_3c_2-a_3b_1c_2+a_3b_2c_1\\ a_1b_2c_3-a_1c_3b_2-a_2b_2c_3+a_2c_3b_2\end{pmatrix}=\begin{pmatrix}a_3b_1c_3-a_1b_3c_3-a_1b_2c_2+a_2b_1c_2\\ a_1b_2c_1-a_2b_1c_1-a_2b_3c_3+a_3b_2c_3\\ a_2b_3c_2-a_3b_2c_2-a_2b_2c_1+a_2c_3b_1\end{pmatrix}$
		- Verknüpfung ist nicht assoziativ => keine Halbgruppe
			- Verknüpfung kann kein Monoid oder abelsche Gruppe werden
- logseq.order-list-type:: number