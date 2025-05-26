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
			- weil $\sum_{k=1}^{\infty}b_{k}$ cauchy ist, gibt es zu jeder $\varepsilon>0$ ein $n\in\mathbb{N}$ mit
			- $$\forall m>l\geq n:\sum_{k=l+1}^{m}\left|a_{k}\right|\leq\sum_{k=l+1}^{m}b_{k}<\varepsilon$$
			- $$\Rightarrow\sum_{k=1}^{\infty}\left|a_{k}\right|\text{ ist cauchy }\Rightarrow\sum_{k-1}^{\infty}a_{k}\text{ konvergiert absolut}$$
		- Minorantenkriterium
		  logseq.order-list-type:: number
			- annahme: $\sum_{k=1}^{\infty}\left|a_{k}\right|$ konvergierte, obwohl $\sum_{k=1}^{\infty}c_{k}$ divergiert
			- $0\leq c_{k}\leq\left|a_{k}\right|$
			- => es wäre $\sum_{k=1}^{\infty}\left|a_{k}\right|$ eine konvergente Majorante von $\sum_{k=1}^{\infty}c_{k}$
			- => Widerspruch
-
- Übung
  collapsed:: true
	- reference:: 4.10
	- sei $\sum_{k=1}^{\infty}a_{k},\sum_{k=1}^{\infty}b_{k},a_{k},b_{k}\in\left(0,\infty\right)$
	- außerdem gilt $q\coloneqq \lim_{k\rightarrow\infty}\frac{a_{k}}{b_{k}}\in\left(0,\infty\right)$
	- Dann gilt: $\sum_{k=1}^{\infty}a_{k}$ konvergiert gdw. $\sum_{k=1}^{\infty}b_{k}$ konvergiert
	- Beweis
		- es gibt einen $n\in\mathbb{N}$ mit $\forall k\geq n:\frac{q}{2}<\frac{a_{k}}{b_{k}}<\frac32q$
		- => $a_{k}<\frac32q\cdot b_{k}$
		- => $\frac{q}{2}b_{k}<a_{k}\Leftrightarrow b_{k}<\frac{q}{2}\cdot a_{k}$
		- "=>"
			- Wenn $\sum a_{k}$ konvergiert, ist die Reihe $\frac{q}{2}\sum a_{k}$ eine konvergente Majorante von $\sum b_{k}$
			- => $\sum_{k=1}^{\infty}b_{k}$ konvergiert
		- "<="
			- $\frac32q\sum b_{k}$ ist eine konvergente Majorante von $\sum a_{k}$
	- Anwendung
		- $a_{k}=\frac{1}{k^2},b_{k}=\frac{1}{k^2+17k+32+\frac{4}{k}}$
		- $$\frac{a_{k}}{b_{k}}=\frac{k^2+17k+31+\frac{4}{k}}{k^2}=1+\frac{17}{k}+\frac{31}{k^2}+\frac{4}{k^3}\longrightarrow{}_{k\rightarrow\infty}1$$
- Übung
  collapsed:: true
	- reference:: 4.11
	- $\sum_{k=1}^{\infty}\frac{1}{k\left(k+1\right)}$ konvergiert
	- Idee: Partialbruchzerlegung
		- $\frac{1}{k\left(k+1\right)}=\frac{\alpha}{k}+\frac{\beta}{k+1}$ mit $\alpha,\beta\in\mathbb{R}$
		- $$\forall k\in\mathbb{N}:\frac{1}{k\left(k+1\right)}=\frac{\alpha}{k}+\frac{\beta}{k+1}\Leftrightarrow0\cdot k+1=\alpha\left(k+1\right)+\beta k$$
		- $$=\alpha k+a+\beta k=\left(\alpha+\beta\right)k+\alpha$$
		- Koeeffizientenvergleich:
		- $$\alpha=1;\alpha+\beta=0$$
		- $$\Rightarrow\alpha=1,\beta=-1$$
		- $$\Rightarrow\forall k\in\mathbb{N}:\frac{1}{k\left(k+1\right)}=\frac{1}{k}-\frac{1}{k+1}$$
		- für $n\in\mathbb{N}$ gilt für die n-k Partialsumme:
		- $$S_{n}=\sum_{k=1}^{n}\frac{1}{k\left(k+1\right)}=\sum\left(\frac{1}{k}-\frac{1}{k+1}\right)=\left(\frac11+\frac12+\frac13+...\right)-\left(\frac12+\frac13+\frac14+...\right)=\frac11-\frac{1}{n+1}$$
		- => Konvergenz: $\lim\sum\frac{1}{k\left(k+1\right)}=1$
-