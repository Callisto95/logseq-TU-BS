- 2025-05-14
	- logseq.order-list-type:: number
	  $$\neg\left\lbrack\left(\left(\neg\neg p\rightarrow\neg r\right)\rightarrow\neg p\right)\land\neg\left\lbrack\left(\neg p\lor\left(r\rightarrow\left(\neg p\land q\right)\right)\right)\land r\right\rbrack\right\rbrack$$
		- Aufteilung:
			- $\neg\left(\left(\neg\neg q\rightarrow\neg r\right)\rightarrow\neg p\right)\Rightarrow\neg\neg q\rightarrow\neg r;\neg\neg p=p$
				- $\neg\neg\neg q=\neg q;\neg r$
			- $\neg\neg\left\lbrack\left(\neg p\lor\left(r\rightarrow\left(\neg p\land q\right)\right)\right)\land r\right\rbrack$
				- $\left(\neg p\lor\left(r\rightarrow\left(\neg p\land q\right)\right)\right)\land r$
					- $\neg p\lor\left(r\rightarrow\left(\neg p\land q\right)\right);r$
						- $\neg p;r\rightarrow\left(\neg p\land q\right)$
							- $\neg r;\neg p\land q=\neg p;q$
	- Sei A eine Formel, sei $\tau\in T_{A}=$"Menge aller Tableus"
	  logseq.order-list-type:: number
		- zZ: Dann gilt: $\forall\phi:\phi\text{ erfüllt A}\Leftrightarrow\exists\Theta\in\tau:\phi\text{ erfüllt }\Theta$
		- sei $\phi$ gegeben
			- "<="
				- $\phi$ erfüllt nach annahme ein $\Theta$, aber $A\in\Theta$, also erfüllt $\phi$ auch A
			- "=>"
				- nach Annahme: $\phi\left(A\right)=1$
				- $A\in\Theta$
				  logseq.order-list-type:: number
					- Konstruiere iterativ ein $\Theta$, indem nur jeder Schritt weitere Formeln zu $\Theta$ hinzufügt
					- also $\Theta=\left\lbrace A_0=A,A_1,A_2,...\right\rbrace$
					- Annahme: $A_0,...,A_{n}$ wurden bereits konstruiert, sodass $\forall i\in\left\lbrack0,n\right\rbrack:\phi\left(A_{i}\right)=1$
					-
				- $A\notin\Theta$
				  logseq.order-list-type:: number