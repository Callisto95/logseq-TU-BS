reference:: VL13

-
- Theorem
	- reference:: 9.17
	- Es sei $f:\mathbb{N}\rightarrow\mathbb{N}$ mit $\forall n:f\left(n\right)\geq\log n$
	- dann gilt $\text{coNSPACE}\left(O\left(f\right)\right)=\text{NSPACE}\left(O\left(f\right)\right)$
	- Beweis:
		- sei $L\in\text{NSPACE}$, also $L=L\left(M\right)$ für eine NTM M
		- zZ: Komplementproblem $\overline{L}$ durch eine $O\left(f\right)$-platzbeschränkte Maschine lösen lässt
		-