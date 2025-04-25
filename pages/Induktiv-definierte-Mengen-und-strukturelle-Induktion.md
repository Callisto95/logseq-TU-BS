- Definition
	- Sei X eine Menge elementarer Bausteine
	- Sei O eine Menge Operation mit Stelligkeit $k\geq1$
	- Die durch X und O induktiv definierte Menge ist die kleinste Menge M mit
	- $X\subseteq M$
	  logseq.order-list-type:: number
	- Falls $o\in O$ mit Stelligkeit k und $m_1,...,m_{k}\in M$ dann gilt auch $o\left(m_1,...,m_{k}\right)\in M$
	  logseq.order-list-type:: number
	- Beispiele
		- $\mathbb{N}:X=\left\lbrace0\right\rbrace,O=\left\lbrace\text{succ}\right\rbrace$ (dabei ist succ=suc/1)
		- $\mathbb{Z}:X=\left\lbrace0\right\rbrace,O=\left\lbrace\text{suc}_1,\text{pred}_1\right\rbrace$
		- $F:X=V,O_{F}=\left\lbrace\neg,\land,\lor,\rightarrow,\Leftrightarrow\right\rbrace$
			- Priorität: $\neg>\land>\lor>\rightarrow>\Leftrightarrow$
-
- Ziel: Beweise $\forall x\in A:P\left(x\right)$, wobei A eine unendliche Menge ist, die aber strukturell Aufgebaut ist
- Intuition:
  collapsed:: true
	- $A:=\left\lbrace0,1,2,3,...\right\rbrace$
	- zeige P(0)
	- zeige für alle Kanten falls P(x), dann P(x+1)
	- => $P\left(0\right)\land\left(P\left(x\right)\rightarrow P\left(x+1\right)\right)\rightarrow\forall x\in\mathbb{N}:P\left(x\right)$
-