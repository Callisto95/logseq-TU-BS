exclude-from-graph-view:: true

- 2025-05-27
  collapsed:: true
	- Zeige TOTALITY ist nicht [[semi-entscheidbar]]
	  logseq.order-list-type:: number
		- $\text{ACCEPT}_{\varepsilon}\leq\text{TOTALITY}$
		- Das Problem: Akzeptiert $M_{w}\space\varepsilon$ nicht, terminiert $M_{w}$ möglicherweise nicht
		- Betrachte $\overline{\text{ACCEPT}_{\varepsilon}}$ etwas anders für w
		- -> $\forall i\in\mathbb{N}:M_{w}\text{ akzeptiert }\varepsilon\text{ nicht in i Schritten}$
		- Betrachte damit Maschine $M_{w^{\prime}}$ mit $w^{\prime}=f\left(w\right)$, die folgendes für ein Wort $x\in\Sigma^{\ast}$ durchführt:
			- Berechne $i=\left|x\right|$
			  logseq.order-list-type:: number
			- Simuliere $M_{w}$ auf $\varepsilon$ für i Schritte
			  logseq.order-list-type:: number
			- Akzeptiert $M_{w}$ nach i Schritten, gehe in Endlosschleife
			  logseq.order-list-type:: number
			- Ansonsten halte
			  logseq.order-list-type:: number
		- zZ: $M_{w}$ akzeptiert $\varepsilon$ nicht $\Leftrightarrow M_{w^{\prime}}$ hält auf jeder Eingabe
			- $w\notin\text{ACCEPT}$, d.h. $M_{w}$ akzeptiert $\varepsilon$ nach $k\in\mathbb{N}$ vielen Schritten
			- -> $M_{w^{\prime}}$ wird in eine endlosschleife gehen, für Wörter $x\in\Sigma^{\geq k}$
			- => $w^{\prime}=f\left(w\right)\notin\text{TOTALITY}$
			- $w^{\prime}\notin\text{TOTALITY}$, dann kann $M_{w^{\prime}}$ nur in eine Endlosschleife geraten, wenn für ein $x\in\Sigma^{\ast}$ die Simulation von $M_{w}$ auf $\varepsilon$ nach $\left|x\right|$ Schritten akzeptiert
			- => $M_{w}\notin\overline{\text{ACCEPT}_{\varepsilon}}$
	- Sei $L_1=\left\lbrace w|\exists x\in L\left(M_{w}\right):\forall y\in\Sigma^{\geq\left|x\right|}:y\in L\left(M_{w}\right)\right\rbrace$
	  logseq.order-list-type:: number
		- Zeige oder Wiederlege: $L_1$ ist (co-)semi-entscheidbar
		- Idee: Zeige $\text{TOTALITY}\leq L_1$
		- Konstruiere $M_{w^{\prime}}$ wie folgt:
			- $M_{w^{\prime}}$ erhält Eingabe $x\in\Sigma^{\ast}$
			- $\forall y\in\Sigma^{\left|x\right|}$:
				- simuliere $M_{w}$ auf y
			- Akzeptiere x
		- Angenommen $w\in\text{TOTALITY}$, dann hält $M_{w}$ auf jeder Eingabe
		- Damit hält die Simulation von $M_{w}$ in $M_{w^{\prime}}$ immer
		- Auch die anderen Schritte sind endlich
		- => $w^{\prime}\in L_1$, da $L\left(M_{w^{\prime}}\right)=\Sigma^{\ast}$
		- ---
		- Angenommen $w\notin\text{TOTALITY}$
		- Dann existiert $y\in\Sigma^{\ast}$, auf dem $M_{w}$ nicht hält
		- Damit hält $M_{w^{\prime}}$ auf keinem $x\in\Sigma^{\ast}$ mit $\left|x\right|\geq\left|y\right|$, d.h. es gibt kein Wort, ab welchem wir alle größeren Wörter akzeptieren
		- => $w^{\prime}\notin L_1$
		- $L_1^{\prime}=\left\lbrace w|\exists x\in L\left(M_{w}\right):\forall y\in\Sigma^{\leq x}:y\in L\left(M_{w}\right)\right\rbrace$
			- nicht co-semi-entscheidbar, aber semi-entscheidbar
			- da $\varepsilon$ auch in $\Sigma^{\leq x}$ muss nur überprüft werden, ob $\varepsilon\in L\left(M_{w}\right)\Rightarrow\text{ACCEPT}_{\varepsilon}$
	- $\text{PCP}_{\equiv r}:\text{wie }0-1-\text{PCP}$
	  logseq.order-list-type:: number
		- [[Postsche-Korrespondenzproblem]]
		- Gegeben: $\left(x_1,y_1\right),...,\left(x_{m},y_{m}\right)$ mit $x_{i},y_{i}\in\left\lbrace0,1\right\rbrace^{\ast}$
		- Gesucht: Eine nicht leere, endliche Sequenz $i_1,...,i_{n}$ mit $n\bmod r=0$
		- Zeige: $0-1-\text{PCP}\leq\text{PCP}_{\equiv r}$
		- Annahme: $I=i_1,...,i_{n}$ ist eine Lösung für PCP mit $n\bmod r=q\in\left\lbrace0,...,r-1\right\rbrace$
			- $I^{r}=IIII...$ ist eine Lösung für PCP mit Länge rn, also $\bmod r=0$
			- => PCP ist nicht Lösbar
			- Ist $\text{PCP}_{\equiv r}$ lösbar, dann ist diese Lösung auch gültig für PCP
		- ---
		- $\text{PCP}_{\leq k}$: wie PCP, nur dass die Lösung höchstenz k Kacheln nutzt
		- -> endlich, also entscheidbar
	- Satz von Rice
	  logseq.order-list-type:: number
		- Seien $a,b\in\Sigma^{\ast}$ und $L_{a,b}=\left\lbrace w|a\in L\left(M_{w}\right)\land b\notin L\left(M_{w}\right)\right\rbrace$
		- Zeige mit Hilfe des Satz von Rice über montone Eigenschaften, dass $L_{a,b}$ weder semi- noch co-semi-entscheidbar ist
		- Betrachte
			- $L_1=\left\lbrace a\right\rbrace\in L_{a,b}$
			- $L_2=\left\lbrace a,b\right\rbrace\notin L_{a,b}$
			- => Eigenschaft ist nicht monoton
				- => nicht semi-entscheidbar
			- $\overline{L_{a,b}}=\left\lbrace w|a\notin L\left(M_{w}\right)\lor b\in L\left(M_{w}\right)\right\rbrace$
			- $L_0=\left\lbrace\varepsilon\right\rbrace\in\overline{L_{a,b}}$
			- $L_1=\left\lbrace a\right\rbrace\notin\overline{L_{a,b}}$
			- => komplement der Eigenschaft ist nicht monoton
				- => nicht co-semi-entscheidbar
	- Speicherbedarf
	  logseq.order-list-type:: number
		- sei $L_2=\left\lbrace w|M_{w}\text{ benötigt für jedes }x\in\Sigma^{\ast}\text{ maximal }|x|^2\text{ gleichzeitig benutzte Zellen}\right\rbrace$
		- -> Speicherbedarf von $M_{w}$
-
- 2025-07-08
	- Problem Clique
		- Gegeben: Graph $G=\left(V,E\right),k\in\mathbb{N}$
		- Frage: $\exists S\subseteq V:\left|S\right|=k,\forall u,v\in S:\left\lbrace u,v\right\rbrace\in E$
		-