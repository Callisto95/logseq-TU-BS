- Grundlagen der Computertechnik
-
- ## logische Funktionen
- AND $\cdot$ (auch $\lor$)
- OR $+$ (auch $\land$)
- NOT $\overline{v}=v^{\prime}=\sim v$
-
- ### Vorrang
- Klammern
  logseq.order-list-type:: number
- NOT
  logseq.order-list-type:: number
- AND
  logseq.order-list-type:: number
- OR
  logseq.order-list-type:: number
-
- ## Dualität
- Vertauschen von $\cdot\Leftrightarrow+$ und $1\Leftrightarrow0$ von einem algebraischen Ausdruck
-
- ### Selbst-Dual
- Wenn $\text{dual H}=\text{H}$, dann ist H selbst-dual
-
- ## Normalformen
- Negation nur auf Eingangsvariablen
- ### DNF
- "Sum of Products"
-
-
- ### KNF
- "Product of Sums"
- dual zur DNF
- Minterm
-
- ### Zusammenhang
- KNF-Erstellung:
	- $\overline{F}$ durch Wahrheitstabelle in DNF bilden
	- De-Morgan Gesetze anwenden um $F$ zu erhalten
-