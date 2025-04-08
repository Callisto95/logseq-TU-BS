- **Ordnungen und Intervalle**
	- es gibt einen Körper $\mathbb{R}=\left(\mathbb{R},+,\cdot\right)$ mit einer Ordnung < mit den Eigenschaften:
		- Verträglichkeit der Ordnung mit der Addition: $\forall a,b,c\in\mathbb{R}:a\leq b\Rightarrow a+c\leq b+c$
		- Verträglichkeit der Ordnung mit der Multiplikation: $\forall a,b,c\in\mathbb{R}:c>0:a\leq b\Rightarrow ac\leq bc$
		- Schnitt-Vollständigkeit: $A,B\subseteq\mathbb{R};A,B\neq\varnothing:R=A\cap B$ und $\forall a\in A,\forall b\in B:a<b$, dann gibt es ein $z\in\mathbb{R}$ mit $a\leq z\leq b$
		  collapsed:: true
			- das ist nicht in $\mathbb{Q}$ möglich
			- "Schnitt" bei $\sqrt2$ -> keine Trennung der beiden Teile, da $\nexists q\in\mathbb{Q}:q^2=2$
		- $\mathbb{R}$ ist somit ein *vollständig angeordneter Körper*
-
- **erweiterte reelle Zahlen**
  collapsed:: true
	- $\hat{\mathbb{R}}:=\mathbb{R}\uplus\left\lbrace\infty\right\rbrace\uplus\left\lbrace-\infty\right\rbrace$
	- $\forall a\in\mathbb{R}:-\infty<a<\infty$
	- Rechenregeln:
		- $\forall a\in\hat{\mathbb{R}}$
		- $a\neq-\infty:a+\infty=\infty$
		  id:: 67f4f429-40a2-458d-8fdb-63f6a8b623d3
		- $a\neq\infty:-\infty+a=-\infty$
		- $0<a\leq\infty:a\cdot\pm\infty=\pm\infty$
		- $-\infty\leq a<0:a\cdot\pm\infty=\mp\infty$
- id:: 67f4f505-35e9-4161-bf7e-cf9ebb027481
- **Intervalle**
	- eine Menge $I\subseteq\mathbb{R}$ heißt (reelles) Intervall, wenn gilt $\forall s,t\in I,\forall r\in\mathbb{R}:s<r<t\Rightarrow r\in I$
	- Arten von Intervallen
		- *offenes Intervall*: $\forall a,b\in\hat{\mathbb{R}};a<b:\left(a,b\right):=\left\lbrace x\in\mathbb{R};a<x<b\right\rbrace$
		- *abgeschlossenes Intervall*: $\forall a,b\in\mathbb{R};a\leq b:\left\lbrack a,b\right\rbrack:=\left\lbrace x\in\mathbb{R};a\leq x\leq b\right\rbrace$
		- *halboffenes Interval*: $\forall a\in\mathbb{R},b\in\hat{\mathbb{R}};a<b:\left\lbrack a,b\right):=\left\lbrace x\in\mathbb{R};a\leq x<b\right\rbrace$
			- auch $a\in\hat{\mathbb{R}},b\in\mathbb{R}$ ist möglich
-