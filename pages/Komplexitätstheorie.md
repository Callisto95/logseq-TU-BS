reference:: 7

- [[Landau-Symbole]]
-
- **Komplexitätsklassen**
	- reference:: 7.2
	- *Zeitverbrauch: Time*
		- $\text{Time}_{M}\left(n\right)=\max\left\lbrace\text{Time}_{M}\left(x\right)|x\in\Sigma^{\ast},n=|x|\right\rbrace$
		- Grundelegende Klassen
			- $\text{DTIME}_{m}\left(f\right)=\left\lbrace L\left(M\right)|\text{M ist eine m-Band DTM und f-zeitbschränkt}\right\rbrace$
			- $\text{NTIME}_{m}\left(f\right)=\left\lbrace L\left(M\right)|\text{M ist eine m-Band NTM und f-zeitbschränkt}\right\rbrace$
				- bei 1-Band TM entfällt Index m
	- *Platzverbrauch: Space*
		- sei c eine Konfiguration von M: $\text{Space}_{M}\left(c\right)=\max\left\lbrace|w|,w\text{ ist der Inhalt eines Arbeitsbandes in Konfiguration c}\right\rbrace$
		- Platzverbrauch zu Eingabe x: $\text{Space}_{M}\left(x\right)=\max\left\lbrace\text{Space}_{M}\left(c\right)|c\text{ ist Konfiguration in einer Berechnung von M zu Eingabe}\right\rbrace$
		- Grundlegende Klassen
			- $\text{DSPACE}_{m}\left(f\right)=\left\lbrace L\left(M\right)|\text{M ist DTM mit read‐ only Eingabe, m Arbeitsbändern, ein Entscheider und f-Platzbeschränkt}\right\rbrace$
			- $\text{NSPACE}_{m}\left(f\right)=\left\lbrace L\left(M\right)|\text{M ist NTM mit read‐ only Eingabe, m Arbeitsbändern, ein Entscheider und f-Platzbeschränkt}\right\rbrace$
		-