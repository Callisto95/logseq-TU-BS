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
	  collapsed:: true
		- Gegeben: Graph $G=\left(V,E\right),k\in\mathbb{N}$
		- Frage: $\exists S\subseteq V:\left|S\right|=k,\forall u,v\in S:\left\lbrace u,v\right\rbrace\in E$
		- zZ: Clique ist NP-Vollständig
			- Möglichkeiten
				- Konstruiere NTM
				  logseq.order-list-type:: number
				- Reduziere auf ein NP Problem
				  logseq.order-list-type:: number
				- Gib einen Zertifizierer an
				  logseq.order-list-type:: number
					- Zertifikat?
					  logseq.order-list-type:: number
					- Überprüfe Zertifikat
					  logseq.order-list-type:: number
			- Beweis durch 3.
				- Produziere Zertifikat $\left\lbrace0,1\right\rbrace^{n}$ für n Knoten
				- Ein Verifizierer überprüft zwei Kriterien
					- Die Anzahl der 1 ist exakt k
					- Für jedes Paar i,j für welche die i-te und j-te Ziffer des Zertifikats eine 1 besitzt, prüfe ob $\left\lbrace v_{i},v_{j}\right\rbrace\in E$
				- Es wurden also k Knoten ausgewählt, die paarweise Verbunden sind
				- Gibt es keine Clique der Größe k, schlägt die Überprüfung immer fehl
		- Problem Clique is NP-schwer: $X\leq_{m}^{\text{poly}}\text{Clique}$
			- Instanz von X -Reduktion f-> Instanz von Clique -Algorithmus-> Lösung von Instanz von Clique -> Lösung für Instanz von X
				- dabei: Instanz von X -deterministischer Algorithmus mindestenz exp->Lösung von X
			- Welches Problem nutzt man für die Reduktion?
				- 3-SAT, Hamiltonkreise, Vertex Cover, Indipendent Set
				- dabei: Clique <=> indipendent Set (= Gegenteil)
				- Idee: Betrachte Graph $\overline{G}=\left(V,\overline{E}\right),\overline{E}=\begin{pmatrix}V\\ 2\end{pmatrix}\backslash E$
				- zZ: G enthält Clique der Größe k gdw. $\overline{G}$ enthält indipendent Set der Größe k
					- "=>"
						- Betrachte Clique S in G der Größe k
						- Da alle Knoten untereinander Verbunden sind, existieren unter S in $\overline{G}$ gar keine Kanten
						- also: S ist ein IS in $\overline{G}$
					- "<="
						- Analog, aber start in $\overline{G}$
				- $$\text{3SAT}\leq^{\text{poly}}\text{VC}\leq^{\text{poly}}\text{IS}\leq^{\text{poly}}\text{Clique}$$
	- Problem "Set Cover"
		- Gegeben $U=\left\lbrace1,...,n\right\rbrace,S\subseteq P\left(U\right),k\in\mathbb{N}$
		- Frage: $\exists C\subseteq S,\left|C\right|=k,\bigcup_{S\in C}S=U$
		- Beispiel
			- $$U=\left\lbrace1,2,3,4,5\right\rbrace,S=\left\lbrace\underline{\left\lbrace1,2,3\right\rbrace},\left\lbrace2,4\right\rbrace,\left\lbrace3,4\right\rbrace,\underline{\left\lbrace4,5\right\rbrace}\right\rbrace$$
			- $$\Rightarrow C=\left\lbrace\left\lbrace1,2,3\right\rbrace,\left\lbrace4,5\right\rbrace\right\rbrace,\left|C\right|=2=k$$
		- zZ: $SC\in NP$
			- Konstruiere NTM
				- Rate, welche Elemente aus S in C liegen (=Rate Zertifikat $\left\lbrace0,1\right\rbrace^{\left|S\right|}$)
				  logseq.order-list-type:: number
				- Überprüfe, ob Auswahl gültig ist:
				  logseq.order-list-type:: number
					- es wurden k Elemente ausgewählt
					  logseq.order-list-type:: number
					- jedes Element aus U kommt in einer Menge in C vor
					  logseq.order-list-type:: number
			- für b:
				- liste alle Elemente aller $S_{i}\in C$ auf, für welche das Zertifikat an i-ter Stelle eine 1 enthält
				- Prüfe für jedes Element in U, ob dieses in der Liste Auftaucht
				- Laufzeit
					- Die Liste enthält maximal $O\left(kn\right)\subset O\left(\left|S\right|n\right)$ viele Elemente
					- Die Überprüfung, ob jedes $u\in U$ vorkommt kann damit in Zeit $O\left(\left|S\right|n^2\right)$ erfolgen
					- Das ist tatsächlich polynomiell im Input ($\left|S\right|+n+\log k$)
				- Korrektheit
					- Wenn es ein Set Cover C der Größe k gibt, dann raten wir an der i-ten Stelle, dass wie Menge $S_{i}$ aufnehmen, wenn $S_{i}\in C$
					- Damit werden k Elemente aus S im Algorithmus gewählt und die Überprüfung muss dadurch gelingen
					- Andernfalls gelingt die Überprüfung in Schritt 2, haben wir k Elemente ausgewählt, die U überdecken -> ist also ein Set Cover der Größe k
		- zZ: SC ist NP-schwer
			- Reduktion $VV$