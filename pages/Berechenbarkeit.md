- Eine (partielle) Funktion $f:\Sigma_1^{\ast}\rightarrow_{p}\Sigma_2^{\ast}$ ist *berechenbar*, wenn es einen Algorithmus gibt, der mit Eingabe $w\in\Sigma_1^{\ast}$
	- nach endlich vielen Schritten akzeptiert und f(w) ausgibt, falls f(w) definiert ist
	- nicht anhält oder nicht akzeptiert, wenn f(w) nicht definiert ist
	  collapsed:: true
		- z.B. unendliche `while true` Schleife
		- ! `return false` **IST** definiert
- Eine Funktion is *effektiv Berechenbar*, wenn man den Algorithmus, welcher die Funktion berechnet, konkret angegeben werden kann
- Ein Entscheidungsproblem ist *effektiv entscheidbar*, wenn man den Entscheidungsalgorithmus für das Problem bekannt ist
-
- Umgekehrt, berechnet jeder (deterministische) Algorithmus eine partielle Funktion
-
- Beispiele
	- Pi-Präfix
	  collapsed:: true
		- $$f_{\pi}\left(n\right):\left\lbrace_{0:\text{ sonst}}^{1:\text{ falls n ein Präfix von pi ist}}\right.$$
		- -> $f_{\pi}\left(314\right)=1,f_{\pi}\left(5\right)=0,f_{\pi}\left(141\right)=0$
		- $f_{\pi}$ ist berechenbar:
			- sei n mit k Ziffern
			- Approximiere $\pi$ auf k-1 Stellen
			- Wenn die Zahlen gleich sind, gib 1 zurück; 0 sonst
	- Pi-Infix
	  collapsed:: true
		- $$g_{\pi}\left(n\right):\left\lbrace_{0:\text{ sonst}}^{1:\text{ falls n ein Infix von pi ist}}\right.$$
		- -> $g_{\pi}\left(314\right)=1,g_{\pi}\left(5\right)=1,g_{\pi}\left(141\right)=1$
		- Unbekannt, ob berechenbar
			- Wie lange muss approximiert werden? -> unbekannt
			- Wenn nicht gefunden wird, dass n ein Infix ist, gibt es keine Abbruchsbedingung
	- P=NP
	  collapsed:: true
		- $$f_{PNP}:\left\lbrace0,1\right\rbrace^{\ast}\rightarrow\left\lbrace0,1\right\rbrace^{\ast};f_{PNP}\left(w\right)\coloneqq \left\lbrace_{1\text{, wenn P\!=NP}}^{0\text{, wenn P=NP}}\right.$$
			- Note: P, NP sind Klassen von Problemen die von DTM / NTM in polynomieller Zeit gelöst werden können (bislang ungelöst).
		- betrachte 2 Algorithmen: $f_1$ gibt immer 1 zurück, $f_0$ gibt immer 0 zurück
		- Einer berechnet $f_{PNP}$, welcher ist aber unbekannt
		-
-
- Es ist nicht möglich alle berechenbare Funktionen aufzuzählen
	- VL04:20
-