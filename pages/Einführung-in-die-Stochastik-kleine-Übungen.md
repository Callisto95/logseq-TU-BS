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
				- $\mathcal{P}\left(\sum_{i=1}^{k}A_1\right)=\sum_{i=1}^{k}\mathcal{P}\left(A_{i}\right)=\sum_{i=1}^{k}\frac{2^{i-1}}{2^{n}}=\frac{1}{2^{n}}\sum_{i=0}^{k-1}2^{i}=\frac{1}{2^{n}}2^{k-1}=\frac{\placeholder{}}{\placeholder{}}$
				-
	- Hashing
	  logseq.order-list-type:: number
		-
	- Geburtstage
	  logseq.order-list-type:: number
		-
	- Olympia
	  logseq.order-list-type:: number
		- logseq.order-list-type:: number