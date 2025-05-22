- $$\mathbb{C}=\left\lbrace x+iy;x,y\in\mathbb{R}\right\rbrace$$
- Besonderheiten:
	- logseq.order-list-type:: number
	  $$i\in\mathbb{C}\setminus\mathbb{R},i^2=-1$$
	- Keine (sinnvolle) Ordnung auf $\mathbb{C}$
	  logseq.order-list-type:: number
		- z.B. 1+i<4+3i macht keinen Sinn
-
- Definition:
	- reference:: 6.1
	- für $z=x+iy\in\mathbb{C};x,y\in\mathbb{R}$ gilt
		- Realteil: $\text{Re}\left(z\right):=x$
		- Imaginärteil: $\text{Im}\left(z\right):=y$
		- komplex Konjugiert: $\overline{z}:=\overline{x+iy}:=x-iy$
		- Betrag: $\left|z\right|:=\left|x+iy\right|:=\sqrt{x^2+y^2}$
		- Abstand: $\left|z-w\right|=\left|x+iy-\left(u+iv\right)\right|=\left|x-u+i\left(y-v\right)\right|=\sqrt{\left(x-u\right)^2+\left(y-v\right)^2}$
			- -> Abstand ist der Verbindungsvektor zwischen $\overrightarrow{z},\overrightarrow{w}$
		- $z\cdot\overline{z}=\left(x+iy\right)\cdot\left(x-iy\right)=x^2-\left(iy\right)^2=x^2+y^2$
			- $\left|z\right|=\sqrt{z\cdot\overline{z}}$
		- $\frac{1}{z}=\frac{1}{z+iy}=\frac{x-iy}{\left(x+iy\right)\cdot\left(x-iy\right)}=\frac{x}{x^2+y^2}-\frac{y}{x^2+y^2}\cdot i$
-
- Korollar: Rechengesetze
	- reference:: 6.2
	- $z=x+iy\in\mathbb{C},w=u+iv\in\mathbb{C}$
	- $\overline{z+w}=\overline{z}+\overline{w}$
	  logseq.order-list-type:: number
	- $\overline{z\cdot w}=\overline{z}\cdot\overline{w}$
	  logseq.order-list-type:: number
	- $\left|z\right|=\sqrt{x^2+y^2}\geq0$
	  logseq.order-list-type:: number
	- $\left|z\right|=0\Leftrightarrow z=0$
	  logseq.order-list-type:: number
-
- Definition
	- reference:: 6.3
	- $\left(z_{n}\right)\subseteq\mathbb{C}$
	- dabei $z_{n}=x_{n}+iy_{n}$ mit $\left(x_{n}\right),\left(y_{n}\right)\subseteq\mathbb{R}$
	- $\left(z_{n}\right)\text{ konvergent}\Leftrightarrow\left(x_{n}\right),\left(y_{n}\right)\text{ beide konvergent}$
	- Dann $\lim_{n\rightarrow\infty}z_{n}=\lim_{n\rightarrow\infty}\left(x_{n}+iy_{n}\right)=\lim_{n\rightarrow\infty}x_{n}+i\cdot\lim_{n\rightarrow\infty}y_{n}$
	- Reihe: $\sum_{k=1}^{\infty}c_{k}\subseteq\mathbb{C}$ mit $c_{k}=a_{k}+ib_{k};a_{k},b_{k}\in\mathbb{R}$
		- wenn $\sum_{k=1}^{\infty}c_{k}\text{ konvergiert}\Leftrightarrow\sum_{k=1}^{\infty}a_{k},\sum_{k=1}^{\infty}b_{k}\text{ beide konvergieren}$
		- Dann $\sum_{k=1}^{\infty}\left(a_{k}+ib_{k}\right)=\sum_{k=1}^{\infty}a_{k}+i\cdot\sum_{k=1}^{\infty}b_{k}$
-
- Definition: absolute Konvergenz
	- reference:: 6.4
	- EIne Reihe $\sum_{k=1}^{\infty}c_{k}\subseteq\mathbb{C},c_{k}=a_{k}+ib_{k}$ ist [[absolute-Konvergenz]], wenn
	  $\sum_{k=1}^{\infty}\left|c_{k}\right|=\sum_{k=1}^{\infty}\sqrt{a_{k}^2+b_{k}^2}$ konvergiert
	- Wegen: $\frac{1}{\sqrt2}\left(\left|a_{k}\right|+\left|b_{k}\right|\right)\leq\sqrt{a_{k}^2+b_{k}^2}\leq\left|a_{k}\right|+\left|b_{k}\right|$
	- => [[Grenzwertsätze-für-Folgen]]\#Majoranten-/Minoranten-kriterium:
		- $$\sum_{k=1}^{\infty}c_{k}\text{ konvergiert absolut}\Leftrightarrow\sum_{k=1}^{\infty}a_{k}$$