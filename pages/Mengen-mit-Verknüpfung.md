- $M$ ist eine Menge
- Eine Abbildung $v:M\times M\rightarrow M$, $(a,b)\mapsto v(a,b)=:a\ast b$ heißt innere, zweistellige Verknüpfung auf $M$
	- $M\times M$: kathesisches Produkt
-
- **Magma**: $(M,\ast)$
	- $\ast$ keine konkrete Verknüpfung, $(M,+)$, $(M,\cdot)$ schon
	- **assoziativ**, wenn $\forall a,b,c\in M:(a\ast b)\ast c=a\ast(b\ast c)$ (Halbgruppe)
	- **kommutativ**, wenn $\forall a,b\in M:a\ast b=b\ast a$ (abelsches Magma)
	- *Beispiel*: Potenzieren
		- Magma $(P,\land)$
		- $\mathbb{N}=\lbrace1,2,3,4,...\rbrace=n\land m:=n^{m}=\prod_{k=1}^{m}n$
		  :LOGBOOK:
		  CLOCK: [2024-10-20 Sun 23:35:45]
		  :END:
		- nicht assoziativ, da: $2^{(1^2)}=2\neq4=(2^1)^2$
		- nicht kommutativ, da: $2^1=2\neq$
- **Halbgruppe**: $\ast$ ist assoziativ
-
- **Monoid**: $e\in M:\forall g\in G:g\ast e=g=e\ast g$
	- $e$ ist das **neutrales Element**
	- $e$ ist **eindeutig**; es gibt nur ein Element $e$
- **Gruppe**: jedes Element g ($g\in M$) besitzt zusätzlich ein rechtsseitig [[Inverses-Element]] ($\forall g\in M:\exists g_{R}\in M:g\ast g_{R}=e$)
-
- **abelsches Magma**: $\ast$ ist kommutativ
	- abelsche Halbgruppe auch möglich ($\ast$ ist assoziativ und kommutativ)