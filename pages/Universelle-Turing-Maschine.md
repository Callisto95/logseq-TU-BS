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
				- Überprüfung, ob v von der Form $v=\prod_{i=0}^{n}\prod_{j=0}^{m}w_{i,j,i^{\prime},j^{\prime},d}$ ist (also Konkatenation korrekt kodierte Transitionen)
				  logseq.order-list-type:: number
					- für jede Kombination aus Zustand und Symbol muss eine entsprechende Kombination existieren
					- Nein: Weise ab
				- Schreibe 0 auf das Zustandsband, denn 0=bin(0) ist die Kodierung des Index des Startzustands $q_0$ von $M_{W}$
				  logseq.order-list-type:: number
				- Schreibe x' auf das Datenband
				  logseq.order-list-type:: number
					- Form von $x^{\prime}=x_1^{\prime}\#x_2^{\prime}\#...\#x_{\left|x\right|}^{\prime}$
					- dabei $x_{i}^{\prime}=1$, wenn $x_{i}=1$ und $x_{i}^{\prime}=10=bin\left(2\right)$, wenn $x_{i}=0$
				- Simuliere die Maschine Schritt für Schritt
				  logseq.order-list-type:: number
					- lese $q_{i}$ vom Zustandsband
					- lese aktuelles Bandsymbol $a_{j}$ vom Datenband
					- suche im Programmband nach der Kodierung $v_{i,j,i^{\prime},j^{\prime},d}$, welche die Transitionsregel $\delta\left(q_{i},a_{j}\right)=\left(q_{i},a_{j},d\right)$ kodiert
					- Ersetze den Inhalt vom Zustandsband durch bin(i')
					- Ersetze Kodierung des aktuellen Bandsymbols bin($a_{i}$) auf den Datenband mit bin($a_{j}$)
-
-
- Theorem 4.6:
	- Man kann eine UTM U konstruieren mit L(U)=ACCEPT
- Theorem 4.9:
	- Das Akzeptanzproblem ACCEPT ist semi-entscheidbar, aber nicht entscheidbar
-