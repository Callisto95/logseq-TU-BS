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