- sei U eine TM mit L(U)=ACCEPT
	- U wird universelle TM (UTM) genannt
	- die codierte TM wird mit Hilfe drei zusätzlicher Bänder: Programm-, Daten-, und Zustandsband
	- Beweis
	  collapsed:: true
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
					- Ersetze Kodierung des aktuellen Bandsymbols bin($a_{j}$) auf den Datenband mit bin($a_{j}^{\prime}$)
					- Bewege den Kopf auf dem Datenband in die durch $d\in\left\lbrace L,R,N\right\rbrace$ spezifizierte Richtung
				- Überprüfe den Inhalt des Zustandsbands bin(i)
				  logseq.order-list-type:: number
					- Akzeptiere, wenn i=1
					- Weise ab, wenn i=2
					- Sonst gehe zurück zu Schritt 5
-
- Theorem 4.6:
	- Man kann eine UTM U konstruieren mit L(U)=ACCEPT
- Theorem 4.9:
	- Das Akzeptanzproblem ACCEPT ist semi-entscheidbar, aber nicht entscheidbar
	- Beweis
	  collapsed:: true
		- Annahme: ACCEPT ist entscheidbar
		- Sei E ein Entscheider mit L(E)=ACCEPT
		- Akzeptanz oder Abweisung von Eingabe w\#x durch E nach endlich vielen Schritten, wenn $x\in L\left(M_{W}\right)$ bzw. $x\notin L\left(M_{W}\right)$
		- Konstruktion von einer weiteren TM D, welche w erwartet und
			- hält und akzeptieren, wenn $w\notin L\left(M_{W}\right)$
			- hält und abweis, wenn $w\in L\left(M_{W}\right)$
		- Konstruktion des Entscheiders D mit Hilfe von E
			- Simulation von E auf der Eingabe w\#w durch D
			- Inversion der Antwort von E
				- Abweisung von E: D akzeptiert
				- Akzeptanz von E: D weist ab
		- Betrachtung von EIngabe $\langle D\rangle$ für Maschine D (D akzeptiert eigene Kodierung)
			- Akzeptanz von $\langle D\rangle$
			  logseq.order-list-type:: number
				- D weist $\langle D\rangle\#\langle D\rangle$ ab
				- da L(E)=ACCEPT -> $\langle D\rangle\notin L\left(D\right)$
			- Abweisung von $\langle D\rangle$
			  logseq.order-list-type:: number
				- D akzeptiert $\langle D\rangle\#\langle D\rangle$ -> $\langle D\rangle\in L\left(D\right)$
			- => Wiederspruch in beiden Fällen
-
- SELF-ACCEPT=$\left\lbrace w\in\left\lbrace0,1\right\rbrace^{\ast};w\in L\left(M_{W}\right)\right\rbrace$
	- Korollar
		- reference:: 4.11
		- SELF-ACCEPT ist semi-entscheidbar, aber nicht entscheidbar
		- Beweis: siehe Theorem 4.9
-