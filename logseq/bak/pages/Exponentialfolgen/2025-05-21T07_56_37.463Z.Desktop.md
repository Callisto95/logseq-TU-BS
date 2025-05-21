reference:: 2.18

- für welche $q\in\mathbb{R}$ konvergiert die Folge $\left(a_{k}\right)_{k=1}^{\infty}$ mit $a_{k}=q^{k}$?
	- Fall 1: $q>1$: f wächst ins unendliche
	- Fall 2: $1>q>0$: f wächst gegen 0
	- Fall 3: $0>q>-1$: wie 2, aber f wechselt zwischen +y und -y
	- Fall 4: $-1>q$: f wächst ins negativ unendliche
	- Fall 5: $q=1$: f = 1
	- Fall 6: $q=-1$: f wechselt zwischen -1 und 1
	- ---
	- a: $q\in\left(-1,1\right):\lim_{k\rightarrow\infty}q^{k}=0$
	  collapsed:: true
		- für $q=0:\forall k\in\mathbb{N}:a_{k}=0$
		- für $q\in\left(-1,1\right)\setminus\left\lbrace0\right\rbrace$: zZ $\forall\epsilon>0:\exists n\in\mathbb{N}:\forall k\geq n:\left|q^{k}-0\right|<\epsilon$
		- -> $\left|q\right|^{k}<\epsilon\Leftrightarrow\left|\frac{1}{q}\right|^{k}>\frac{1}{\epsilon}$
		- $\tilde{q}:=\left|\frac{1}{q}\right|>1,s:=\frac{1}{\epsilon}$
		- $\left|\frac{1}{q}\right|=1+x$ mit $x:=\left|\frac{1}{q}\right|-1>0$
		- *Bernulli*: $\left|\frac{1}{q}\right|^{k}=\left(1+x\right)^{k}\geq1+kx>^{!?}\frac{1}{\epsilon}$
		- $\Leftrightarrow k>\frac{1}{x}\left(\frac{1}{\epsilon}-1\right)$
		- *Archimedes*: $n\in\mathbb{N}$ mit $n>\frac{1}{x}\left(\frac{1}{\epsilon}-1\right)$
		- also $k\geq n$
	- b: $q=1:\lim_{k\rightarrow\infty}q^{k}=1$
	- c: $q\in\mathbb{R}\setminus\left(-1,1\right\rbrack:\lim_{k\rightarrow\infty}q^{k}\text{divergiert}$
	  collapsed:: true
		- für $q=-1:\left(a_{k}\right)=\left(\left(-1\right)^{k}\right)$ -> divergiert
		- für $\left|q\right|>1$ reicht es nach Satz 2.17 zZ: $\left(q^{k}\right)_{k=1}^{\infty}$ ist unbeschränkt
		- Annahme zwecks Widerspruch: $\exists s\in\left(0,\infty\right):\forall k\in\mathbb{N}:\left|q^{k}\right|\leq s$
		- Schreibe $\left|q\right|=1+x$ mit $x:=\left|q\right|-1>0$
		- => $\left|q^{k}\right|=\left|q\right|^{k}=\left(1+x\right)^{k}\leq s$
		- *Bernulli*: $\left(1+x\right)^{k}\geq1+kx$
		- => $s\geq\left(1+x\right)^{k}\geq1+kx$
		- => $\forall k\in\mathbb{N}:1+kx\leq s$
			- $kx\leq s-1$
			- $k\leq\frac{s-1}{x}$
			- => *Archimedes*: alle $\mathbb{N}$ sind unbeschränkt, aber k ($\forall k\in\mathbb{N}$) wird beschränkt