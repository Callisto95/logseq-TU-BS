- 1: 2025-04-17
	- Binary Search
	  logseq.order-list-type:: number
		- $\Omega=\left\lbrace0,...,2^{n-1}\right\rbrace$, also $\left|\Omega\right|=2^{n}$
		- $\omega\in\Omega$ Platznummer des Schlüsselelementes
			- bei $\omega=0$ ist das gesuchte Element nicht vorhanden
		- Was ist die Wahrscheinlichkeit, dass in k Schritten das Schlüsselelement gefunden wird?
			- $A_1=\left\lbrace2^{n-1}\right\rbrace$
			- $A_2=\left\lbrace2^{n-2},3\cdot2^{n-2}\right\rbrace$
			- Allgemein: $A_{k}=\left\lbrace\left(2j-1\right)\cdot2^{n-k},j\in\left\lbrace1,2,...,2^{k-1}\right\rbrace\right\rbrace,k=1,...,n$
			- $\left|A_{k}\right|=2^{k-1}$
			- Annahme: Laplace-Raum: $\mathcal{P}\left(A_{k}\right)=\frac{\left|A_{k}\right|}{\left|\Omega\right|}=\frac{2^{k-1}}{2^{n}}=2^{k-n-1}$
				- $$\mathcal{P}\left(\sum_{i=1}^{k}A_1\right)=\sum_{i=1}^{k}\mathcal{P}\left(A_{i}\right)=\sum_{i=1}^{k}\frac{2^{i-1}}{2^{n}}=\frac{1}{2^{n}}\sum_{i=0}^{k-1}2^{i}=\frac{1}{2^{n}}2^{k-1}=\frac{2^{k-1}}{2^{n}}$$
	- Hashing
	  logseq.order-list-type:: number
		- $\Omega=\left\lbrace\left(i_1,...,i_{a}\right):i_1,...,i_{a}\in\left\lbrace1,...,n\right\rbrace\right\rbrace;k\leq n$
		- $\left|\Omega\right|=n^{k}$ (ziehen mit zurücklegen)
		- A=mindestenz eine Kollision
		- $\overline{A}$=keine Kollision
		- $\left|\overline{A}\right|=n\cdot\left(n-1\right)\cdot...\cdot\left(n-k+1\right)$
		- $$\mathcal{P}\left(\overline{A}\right)=\frac{\left|\overline{A}\right|}{\left|\Omega\right|}=\frac{n\cdot\left(n-1\right)\cdot...\cdot\left(n-k+1\right)}{n^{k}}=1\cdot\left(1-\frac{1}{n}\right)\cdot\left(1-\frac{2}{n}\right)\cdot...\cdot\left(1-\frac{k-1}{n}\right)$$
		- dabei $\mathcal{P}\left(A\right)=1-\mathcal{P}\left(\overline{A}\right)$
	- Geburtstage
	  logseq.order-list-type:: number
		- Annahme: Laplace-Raum für Tage
		  id:: 6800ffac-a264-488d-92d1-c0b195ab81e6
		- $\Omega=\left\lbrace\left(i_1,...,i_{n}\right):i_1,...,i_1\in\left\lbrace1,...,365\right\rbrace\right\rbrace;n\leq365$
		- A=mindestenz 2 Person haben am gleichen Tag Geburtstag
		- $\overline{A}$=alle haben an unterschiedlichen Tagen Geburtstag
		- $\left|\overline{A}\right|=365\cdot364\cdot...\cdot\left(365-n+1\right)$
		- $$\mathcal{P}\left(\overline{A}\right)=\frac{\left|\overline{A}\right|}{\left|\Omega\right|}=\frac{365\cdot...\cdot\left(365-n+1\right)}{365^{n}}=1\cdot\left(1-\frac{1}{365}\right)\cdot...\cdot\left(1-\frac{n-1}{365}\right)$$
	- Olympia
	  logseq.order-list-type:: number
		- WR: $\Omega=\left\lbrace\omega=\left(\omega_1,...,\omega_7\right):\omega_{i}\in\left\lbrace0,...,9\right\rbrace,i=1,...,7\right\rbrace$
		- Gewinnzahlen
		  logseq.order-list-type:: number
			- $$\mathcal{P}\left(\omega=\left(1,2,3,4,5,6,7\right)\right)=\frac{7}{70}\cdot...\cdot\frac{7}{64}=\frac{7^7}{\begin{pmatrix}70\\ 63\end{pmatrix}\cdot7!}$$
			- dabei: $\begin{pmatrix}70\\ 63\end{pmatrix}\cdot7!=70\cdot...\cdot64$
			- $$\mathcal{P}\left(\omega=\left(7,7,7,7,7,7,7\right)\right)=\frac{7}{70}\cdot...\cdot\frac{1}{64}=\frac{7!}{\begin{pmatrix}70\\ 63\end{pmatrix}\cdot7!}=\frac{1}{\begin{pmatrix}70\\ 63\end{pmatrix}}$$
		- 3143643
		  logseq.order-list-type:: number
			- $$\mathcal{P}\left(w=\left(3,1,4,3,\right)\right)$$
		- fair?
		  logseq.order-list-type:: number
			- Kombinationen mit einzigartigen Zahlen, wie 1234567, sind wahrscheinlicher als Kombinationen mit der selben Zahl mehrmals
-