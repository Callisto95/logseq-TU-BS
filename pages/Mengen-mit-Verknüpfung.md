- $M$ ist eine Menge
- Eine Abbildung $v:M\times M\rightarrow M$, $(a,b)\mapsto v(a,b)=:a\ast b$ heißt innere, zweistellige Verknüpfung auf M
	- $M\times M$: kathesisches Produkt
- **Magma**: $(M,\ast)$
  collapsed:: true
	- $\ast$ keine konkrete Verknüpfung, $(M,+)$, $(M,\cdot)$ schon
	- **assoziativ**, wenn $\forall a,b,c\in M:(a\ast b)\ast c=a\ast(b\ast c)$
	- **kommutativ**, wenn $\forall a,b\in M:a\ast b=b\ast a$
	- *Beispiel*: Potenzieren
	  collapsed:: true
		- $\mathbb{N}=\lbrace1,2,3,4,...\rbrace=n\land m:=n^{m}=\prod_{k=1}^{m}n$
		  :LOGBOOK:
		  CLOCK: [2024-10-20 Sun 23:35:45]
		  :END:
		- nicht assoziativ, da: $2^{(1^2)}=2\neq4=(2^1)^2$
		- nicht kommutativ, da: $2^1=2\neq$
- **Halbgruppe**: $\ast$ ist assoziativ
- **Monoid**: $e\in M:\forall g\in G:g\ast e=g=e\ast g$
  collapsed:: true
	- $e$ = neutrales Element
- **Gruppe**: jedes Element g ($g\in M$) besitzt ein rechtsseitig inverses Element ($\forall g\in M:\exists g_{R}\in M:g\ast g_{R}=e$)
	- **abelsche Gruppe**: $\ast$ ist kommutativ
		- abelsche Halbgruppe auch möglich ($\ast$ ist assoziativ und kommutativ)
-