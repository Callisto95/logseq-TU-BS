- Satz: **Majoranten- und Minorantenkriterium**
	- reference:: 4.9
	- Sei $\left(S_{n}\right)=\sum_{k=1}^{\infty}a_{k}\subseteq\mathbb{R}$ eine [[Reihe]]
	- **Majorantenkriterium**
	  logseq.order-list-type:: number
		- Wenn es eine konvergente Reihe $\sum_{k=1}^{\infty}b_{k}\subseteq\mathbb{R}$ mit $\forall k\in\mathbb{N}:\left|a_{k}\right|\leq b_{k}$ gibt, dann konvergiert $\left(S_{n}\right)$ absolut
			- = *konvergente Majorante*
	- **Minorantenkriterium**
	  logseq.order-list-type:: number
		- Wenn es eine divergente Reihe $\sum_{k=1}^{\infty}c_{k}\subseteq\mathbb{R}$ mit $\forall k\in\mathbb{N}:\left|a_{k}\right|\geq c_{k}\geq0$ gibt, dann konvergiert $\left(S_{n}\right)$ *nicht absolut*
			- = *divergente Minorante*
		- Falls $a_{k}\geq0:\sum_{k=1}^{\infty}a_{k}$ divergiert
	- Beweis
		- Majorantenkriterium
		  logseq.order-list-type:: number
			- weil $\sum_{k=1}^{\infty}b_{k}$ cauchy ist, gibt es zu jeder $\epsilon>0$ ein $n\in\mathbb{N}$ mit
			- $$\forall m>l\geq n:\sum_{k=l+1}^{m}\left|a_{k}\right|\leq\sum_{k=l+1}^{m}b_{k}<\epsilon$$
			- $$\Rightarrow\sum_{k=1}^{\infty}\left|a_{k}\right|\text{ ist cauchy }\Rightarrow\sum_{k-1}^{\infty}a_{k}\text{ konvergiert absolut}$$
		- Minorantenkriterium
		  logseq.order-list-type:: number
			- annahme: $\sum_{k=1}^{\infty}\left|a_{k}\right|$ konvergierte, obwohl $\sum_{k=1}^{\infty}c_{k}$ divergiert
			- $0\leq c_{k}\leq\left|a_{k}\right|$
			- => es wäre $\sum_{k=1}^{\infty}\left|a_{k}\right|$ eine konvergente Majorante von $\sum_{k=1}^{\infty}c_{k}$
			- => Widerspruch
-