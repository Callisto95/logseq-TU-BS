alias:: Funktionen

-
- sei M eine Menge
- Dann wird die Menge $Map(M,M)$ aller Abbildungen von M nach M durch die Verkettung als Verknüpfung zu einem Monoid
- neutrales Element $I_{M}$, $\forall x\in M:I_{M}(x)=x$
- Einheitengruppe des neutralen Elements / der Menge (> undeutlich **???**)
	- $Perm\ M:=(Map(M,M))^{\times}=\lbrace f:M\rightarrow M\rbrace$, wobei f *bijektiv* ist (eindeutige umwandlung)
		- $\mathbb{F}=f^{-1}$ (Umkehrfunktion, möglich da $f$ eindeutig)
		- nicht kommutativ
	- ist mit der gleichen Verknüpfung eine (i.A. nicht abelsche) Gruppe
	- = Permutationsgruppe (bzw. symmetrische Gruppe) von M
-
- Beispiel
	- $\mathbb{Z}\subseteq\mathbb{Q}$
	- beide Mengen bilden mit der Addition eine Gruppe
-
-
-
- Seien A,B zwei Mengen
- Eine Abbildung $f:A\rightarrow B$ ist eine Vorschrift, die jedem Element aus A genau ein Element aus B zuordnet
	- $f:A\rightarrow B:a\mapsto f(a)$
	- $Abb(A,B)$ Menge aller Abbildungen von A nach B
-
- A heißt Definitionsbereich von f
- B heißt Wertebereich von f
- Eine Abbildung besteht aus drei Teilen
	- Definitionsbereich A
	  logseq.order-list-type:: number
	- Wertebereich B
	  logseq.order-list-type:: number
	- Zuordnungsvorschrift $a\mapsto f(a)$
	  logseq.order-list-type:: number
	- Zwei Abbildung sind nur gleich, wenn alle drei Eigenschaften Übereinstimmen
- Zu $a\in A$ heißt f(a) Bild von a unter f
- $f(a)=\lbrace f(a)|a\in A\rbrace$ heißt Bild von f
- Zu $b\in B$ heißt $f^{-1}(b)=\lbrace a\in A|f(a)=b\rbrace$ **Urbild** von b unter f
- Beispiel
	- $f:\mathbb{Z}\rightarrow\mathbb{N_0}:x\mapsto x^2$
	- $A=\mathbb{Z}$ Definitionsbereich
	- $B=\mathbb{N}_0$ Wertebereich
	- $f(A)=\lbrace y\in\mathbb{N}_0|y\ ist\ ein\ Quadrat\rbrace\subseteq\mathbb{N}_0$
	- $f^{-1}(1)=\lbrace1,-1\rbrace$
	- $f^{-1}(2)=\varnothing$
		- "dieses Element gibt es nicht" ist keine Antwort; eine Menge muss vorhanden sein
-