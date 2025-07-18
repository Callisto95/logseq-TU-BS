- (Typen beziehen sich auf die Chomsky-Hierarchie)
- Typ 0 Grammatik G:
	- $G=\left(N,\Sigma,P,S\right)$, wobei $P\subseteq\left(N\cup\Sigma\right)^{\ast}\times\left(N\cup\Sigma\right)^{\ast}$
- Typ 1 Grammatik G / **kontextsensitive Grammatik**
	- G ist kontextsensitiv, wenn für alle Produktionen $a_1\rightarrow a_2$ gilt $\left|a_1\right|\leq\left|a_2\right|$
	- Dabei ist $S\rightarrow\varepsilon$ erlaubt, solange S nicht auf der rechten Seite einer Produktion ist
- Eine Sprache L ist kontextfrei, wenn es eine CFG gibt mit $L\left(G\right)=L$
- Eine Sprache ist **rekursive aufzählbar**, wenn es eine Typ-0 CFG mit $L\left(G\right)=L$ existiert
-
- $w\in L\left(G\right)$ kann nur in exponentieller Zeit gelöst werden
	- alle Wörter der Länge $l\leq\left|w\right|$ müssen getestet werden
-