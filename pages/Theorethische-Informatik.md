- [[Theorethische-Informatik-Übungen]]
-
- Syntax und Semantik von Programmiersprachen
- Automaten und formale Sprachen
-
- [code1] || [code2] = paralleler Code
- DRF-Guarantee (Data Race Free Guarantee)
	- Wenn das Programm ohne synchronisierten Zugriff ist, dann ist der shared memory wie sequenzieller Speicher
-
- [[Partielle-Ordnung]]
- [[Schranken]]
- [[Verband]]
-
- *Unvergleichbarkeit*
  collapsed:: true
	- Beispiel: Teilmengen von $\lbrace0,1,2,3\rbrace$
		- ![image.png](../assets/image_1729590536561_0.png)
		- $\lbrace1\rbrace$ und $\lbrace3\rbrace$ sind unvergleichbar
	- Beispiel: Teiler von 12
		- "->" entspricht "teilt"
		- ![image.png](../assets/image_1729590486443_0.png)
		- 2 und 3 sind unvergleichbar
-
- **monotone Funktionen**
  collapsed:: true
	- $(D,\leq)$ (partielle Ordnung)
	- $f:D\rightarrow D$ ist monoton, wenn $\forall x,y\in D:x\leq y\Rightarrow f(x)\leq f(y)$
	- **Stetigkeit**
		- $(D,\leq)$ vollständiger Verband
		- eine Funktion $f:D\rightarrow D$ heißt
			- $\sqcup$-stetig (**aufwärtsstetig**), falls für jede $K\subseteq D$ gilt: $f(\sqcup K)=\sqcup f(K)=\sqcup\lbrace f(k)|k\in K)\rbrace$
			- $\sqcap$-stetig (**abwärtsstetig**), falls für jede $K\subseteq D$ gilt: $f(\sqcap K)=\sqcap f(K)=\sqcap\lbrace f(k)|k\in K)\rbrace$
	- Beispiel
		- $x,y\in D$ mit $x\sqsubseteq y$
		- sei $x^{\prime}\coloneqq x\sqcap keep$ und $y^{\prime}\coloneqq y\sqcap keep$
		- da $x\sqsubseteq y$ ist also x' auch eine untere Schranke von y
-
- [[Fixpunkte]]
- [[Kette]]
-
- **Satz von Kaster und Tarski**
  collapsed:: true
	- $(D,\leq)$ vollständiger [[Verband]]
	- $f:D\rightarrow D$ monotone Funktion
	- $\sqcap Prefix(f)$ ist der eindeutig kleinster Fixpunkt von f
	  logseq.order-list-type:: number
		- $kfp(f)$ oder auch $\mu f$
	- $\sqcup Postfix(f)$ ist der eindeitig größter Fixpunkt von f
	  logseq.order-list-type:: number
		- $gfp(f)$ oder auch $\nu f$
- **Satz von Klenee**
  collapsed:: true
	- $(D,\leq)$ vollständiger Verband
	- $f:D\rightarrow D$ monoton
	- falls  f $\sqcup$-stetig $lfp(f)=\sqcup\lbrace f^{i}(\bot):i\in\mathbb{N}\rbrace$
	- falls  f $\sqcap$-stetig $gfp(f)=\sqcap\lbrace f^{i}(\top):i\in\mathbb{N}\rbrace$
-
- Erreichbare Knoten in einem Graph
  collapsed:: true
	- $G=(V,E)$
	- $v_1\leftrightarrow v_2\rightarrow v_3\ \ v_4$
	- Verband $(\mathbb{P}(V),\leq)$
	- Funktion $f:\mathbb{P}(V)\rightarrow\mathbb{P}(V)$
		- $X\mapsto X\cup\lbrace v_1\rbrace\cup post(x)$
			- $post(x)\coloneqq \lbrace v^{\prime}\in V|\exists v\in X:v\rightarrow v^{\prime}\in E\rbrace$ (alle Nachfolgerknoten in X)
	- Ziel: $\lbrace v_1,v_2,v_3\rbrace$
	- ist der Satz von Klenee anwendbar?
		- Potenzmengen sind vollständig und endlich
		- Funktion f ist monoton
			- $\forall X,Y\in V:X\subseteq Y\Rightarrow f(X)\subseteq f(Y)$
			- monotonie gilt: sei $X\subseteq Y$: Zeige $f(X)\subseteq f(Y)$
			- $=[X\cup\lbrace v_1\rbrace\cup post(X)]\subseteq[Y\cup\lbrace v_1\rbrace\cup post(Y)]$
			-
			- Sei $a\in f(X)$
			- Zeige $a\in f(X)$
				- $a\in X$, dann $a\in Y\subseteq f(Y)$
				  logseq.order-list-type:: number
				- $a=v_1$, dann $a\in f(Y)$
				  logseq.order-list-type:: number
				- $a\in post(X)$, dann gibt es $c\in X:c\rightarrow a\in E$. Da $X\subseteq Y$ gibt es $c\in Y$ mit $c\rightarrow a\in E$. Also $a\in post(Y)$
				  logseq.order-list-type:: number
-