exclude-from-graph-view:: true

- 2025-05-27
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
		- Damit hält die Simulation von $M_{w}$ i