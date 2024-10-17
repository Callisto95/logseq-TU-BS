- Eine Aussage ist eine Äußerung, der man einen Wahrheitswert zugeordnet werden kann.
	- W: Wahr (1)
	- F: Falsch (0)
- Zweiwertigkeit: Eine Aussage ist entweder Wahr oder Falsch.
- Keine Variablen (einfache Aussagenlogik), deren Belegung den Wahrheitswert beeinflusst.
- Aussagenvariablen werden verwendet
	- Wenn es Regnet (A), dann wird die Erde nass (B).
		- A => B
		- dabei sind A und B boolsche Variablen; "=>" ist eine Operation
- Operationen der Aussagenlogik:
	- Negation: $\neg P$
	- Konjunktion: $P \land Q$
	- Disjunktion: $P \lor Q$
	- Implikation: $P \implies Q$: Wenn P gilt, dann auch Q
	- Äquivalenz: $P \iff Q$: P gilt genau dann, wenn Q gilt
- Wahrheitstabellen:
	- Klärung von Fragen / Aussagen
	- |P|Q|$P \implies Q$|$P \iff Q$|
	  |--|--|--|--|
	  |0|0|1|1|
	  |0|1|1|0|
	  |1|0|0|0|
	  |1|1|1|1|
		- Beispiel:
		- |A|B|$A \implies B$|$\neg A \implies \neg B$|
		  |--|--|--|--|
		  |0|0|1|1|
		  |0|1|1|1|
		  |1|0|0|0|
		  |1|1|1|1|
		- $A \implies B$ und $\neg A \implies \neg B$ sind logisch äquivalent
	- $\neg, \lor, \land, \implies, \iff$ sinf Junktoren
	- $\lor$ ist nicht exlusiv
	- bei $P \implies Q$ heißt P die Prämisse und Q die Konklusion
	- Eine