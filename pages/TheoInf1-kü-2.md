exclude-from-graph-view:: true

-
- n1=24,n2=18,n3=12
  logseq.order-list-type:: number
	- 5184
	- x=3: kgv(18,60)=180 (10,3)
	- ggt(24,180)=12
	-
	- sei $x,y\in D:x\leq y:f(x)\leq f(y)$ (genauer?)
		- $x\leq y$ und $y\leq x$, dann $x=y:f(x)=f(y)$
	-
	- sei x das kleinste Elemente in fa
		- y soll ein kleineres Element sein
		- y ist dann ein kleinerer Teiler von n1 und kgv
		- durch ggt wird aber nur der größte Teiler verwendet, wodurch y nicht in der Menge von fa enthalten ist
- -
  logseq.order-list-type:: number
- Nicht-Join-Stetigkeit
  logseq.order-list-type:: number
	- $x\leq^{w}y$ wenn
		- $x\leq y$
		- $x\neq w+1\land y=w$
		- $y=w+1$
		-
		- x ist mit einem größeren y in Relation
		- alle x sind mit w in Relation, solange $x\neq w+1$
			- -> w ist mit w in Relation
		- alles ist mit w+1 in Relation
		- $(x,y)\leq(x\neq w,w)\leq(x,w+1)$
	-
	- monotonie
		- sei x=w, y=w+1, dann f(x)=w+1;f(y)=w+1 => $f(x)\leq f(y)$
		- sei $x,y\in\mathbb{N}:x\leq y:f(x)=x\leq y=f(y)$
	- Join-Stetigkeit
		- $\sqcup-stetig:K\subseteq D:f(\sqcup K)=\sqcup f(K)$
		- $\sqcup K=w\Rightarrow f(\sqcup K)=w+1$
		-