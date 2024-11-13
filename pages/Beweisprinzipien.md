- $P_1\land...\land P_{r}\Rightarrow Q$
- P: Voraussetzungen, Q Aussage
-
- **Kontraposition**
	- Verwendung von $P\Rightarrow Q$, wodurch $\neg P\Rightarrow\neg Q$
-
- **Wiederspruchsbeweis**
	- $P=P_1\land...\land P_{n}\Rightarrow Q$
	- nehme an Q gilt nicht
	- ein $P_{i}$ muss daher nicht gelten / nicht wahr sei
-
- **Vollständige Induktion**
	- Aussage S(n) für alle natürlichen Zahlen
	- $n\geq n_0$
	- Anfang: Zeige, dass S für das kleinste $n_0$ wahr ist
	  logseq.order-list-type:: number
	- Voraussetzung: Aussage S(n) ist wahr für ein $n\in\mathbb{N}:n\geq n_0$ (n beliebig, aber fest)
	  logseq.order-list-type:: number
	- Induktion: Beweis von S(n+1) unter Verwendung von S(n)
	  logseq.order-list-type:: number
	- Beispiele
		- logseq.order-list-type:: number
			- $\sum_{i=1}^{n}i^3=\frac{n^2(n+1)}{4}$
			- Induktionsanfang: für $n=1:1^3=1=\frac{1^2\cdot2^2}{4}$
			- Induktionsvoraussetzung: Die Aussage gilt für ein beliebiges, aber festes $n\in\mathbb{N}$
			- Induktionsschritt: Zeigen, dass die Aussage n+1 gilt: $\sum_{i=1}^{n+1}i^3=\sum_{i=1}^{n}i^3+(n+1)^3=IV=\frac{n^2(n+1)^2}{4}+(n+1)^3=\frac{(n+1)^2(n+2)^2}{4}$
		- logseq.order-list-type:: number
			- $\sum_{i=0}^{n}q^{i}=\frac{q^{n+1}-1}{q-1}$ für $q\in\mathbb{R}\setminus\lbrace0,1\rbrace$
-
- **starke vollständige Induktion**
	- Anfang: Beweis für $S(n_0)$
	  logseq.order-list-type:: number
	- Voraussetzung: S(k) ist wahr für alle $k\in\mathbb{N}:n_0\leq k\leq n$ ($n\geq n_0$ kleiner aber fest)
	  logseq.order-list-type:: number