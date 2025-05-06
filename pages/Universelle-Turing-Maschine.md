- sei U eine TM mit L(U)=ACCEPT
	- U wird universelle TM (UTM) genannt
	- die codierte TM wird mit Hilfe drei zusätzlicher Bänder: Programm-, Daten-, und Zustandsband
	- Beweis (I guess)
		- Betrachte Eingabe w\#x
			- Überprüfung, ob w eine valide Kodierung einer TM ist
				- falls nicht, dann $M_{W}=M_{\varnothing}$ und es gilt $x\notin L\left(M_{W}\right)$ (-> U lehnt ab)
			- Simulation von $M_{W}$ auf Eingabe x Schritt für Schritt
				- Überprüfung, ob w das Bild eines Wortes $v\in\left\lbrace0,1,\#\right\rbrace^{\ast}$ gemäß des Homomorphismus ist
				  logseq.order-list-type:: number
					- Ja: Speicherung von v auf dem Programmband
					- Nein: Weise ab
				- Überprüfung, ob v von der Form $v=\prod_{i=0}^{n}\prod_{j=0}^{m}w_{i,j,i^{\prime},j^{\prime},d}$ ist
				  logseq.order-list-type:: number
-
- Theorem 4.6:
	- Man kann eine UTM U konstruieren mit L(U)=ACCEPT
- Theorem 4.9:
	- Das Akzeptanzproblem ACCEPT ist semi-entscheidbar, aber nicht entscheidbar
-