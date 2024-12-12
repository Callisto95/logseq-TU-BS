reference:: 2.5

- Eine Rekursionsgleichung der Form $f_{n}=a_1f_{n-1}+...+a_{r}f_{n-r}+g\left(n\right)$ (*a*) mit $1\leq r\leq n,a_1,...,a_{n}\neq0$ heißt lineare Differenzengleichung der Ordnungsgröße
	- homogen: $\forall n\in\mathbb{N}:g\left(n\right)=0$
	- inhomogen: $\forall n\in\mathbb{N}:g\left(n\right)\neq0$
-
- Durch Vorgabe von r Anfangswerten $f_{a},...,f_{r-1}$ ist $\left(f_{a}\right)_{n\in\mathbb{N}0}$ eindeutig bestimmt
- Man nennt $f_{n}=a_1f_{n-1}+...+a_{r}f_{n-r}$ (*b*) die zu (*a*) homogene Gleichung
-
- 2.34: Man nennt $q^{r}-a_1q^{r-1}-...-a_{r-1}q-a_{r}$ das characteristische Polynom zu (*b*)
-
- 2.35: Der *Fundamentalsatz der Algebra* besagt, dass die Gleichung $q^{r}-a_1q^{r-1}-...-a_{r-1}q-a_{r}=0$ genau r Lösungen in $\mathbb{C}$ besitzt: $q_1,...,q_{r}$
-
- 2.36: Sei $\frac{s}{t}\in\mathbb{Q}$ Nullstelle von $a_{n}x^{n}+...+a_1x+a_0$ mit $s,t,a\in\mathbb{Z}$ und s,t teilerfremd
	- Dann gilt: $s|a_0$ und $t|a_{n}$
	- ist $a_{n}=1$, so sind alle Nullstellen aus $\mathbb{Q}$ schon in $\mathbb{Z}$ und Teiler von $a_0$
	-