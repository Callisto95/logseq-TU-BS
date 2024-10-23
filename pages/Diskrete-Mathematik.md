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
- Wahrheitstabellen
	- Klärung von Fragen / Aussagen
	- collapsed:: true
	  |P|Q|$P \implies Q$|$P \iff Q$|
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
	- Eine itoierte Verknüpfung von Variablen heißt boolsche Formel / boolscher Ausdruck.
- Bei der Belegung der Aussagenvariablen mit Wahrheitswerten erhält eine boolsche Formel einen Wahrheitswert.
-
- Vereinbarung
	- $\neg$ bindet stärker als $\land$ und $\lor$
	- $\lor$ und $\land$ binden stärker als $\iff$ und $\implies$
-
- Arten von boolschen Formeln
	- Eine boolsche Formel heißt *erfüllbar*, falls es eine Belegung der Variablen gibt, sodass die Formel Wahr ist.
	- Eine boolsche Formel heißt *Kontradiktion*, wenn sie bei allen möglichen Belegungen falsch ist.
	- Eine boolsche Formel heißt *Tautologie*, wenn sie unter allen möglichen Belegungen Wahr ist.
-
- Zwei Formeln $F_1$ und $F_2$ heißen *Äquivalent*, wenn in der Wahrheitstabelle von $F_1$ und $F_2$ die gleichen Werte stehen (wenn $F_1 \iff F_2$).
	- => $F_1 \sim F_2$ oder $F_1 \equiv F_2$