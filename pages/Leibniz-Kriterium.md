reference:: 4.5

- Sei $\left(a_{k}\right)\subseteq\mathbb{R}$ eine monotone Nullfolge
- Die Reihe $\sum_{k=1}^{\infty}\left(-1\right)^{k}a_{k}$ konvergiert
- Beweis
  collapsed:: true
	- Die Folge $\left(a_{k}\right)$ sei oBdA monoton fallend
	- => $a_{k}\geq0$
	- Zerlege $\left(S_{k}\right)$ in zwei Teilfolgen: $\left(S_{2n}\right),\left(S_{2n-1}\right)$
	- Beide Folgen sind monoton
	- $$\left(S_{2n}\right):S_{2\left(n+1\right)}=S_{2n+2}=\sum_{k=1}^{2n+2}\left(-1\right)^{k}a_{k}=\sum_{k=1}^{2n}\left(-1\right)^{k}a_{k}+\left(-a_{2n+1}+a_{2n+2}\right)\leq S_{2n}$$
	- fällt monoton
	- $$\left(S_{2n-1}\right):S_{2\left(n+1\right)-1}=\sum_{k=1}^{2n+1}\left(-1\right)^{k}a_{k}=\sum_{k=1}^{2n-1}\left(-1\right)^{k}a_{k}+\left(a_{2n}-a_{2n+1}\right)\geq S_{2n-1}$$
	- steigt monoton
	- Außerdem: $S_{2n}-S_{2n-1}=a_{2n}\geq0\Rightarrow S_1\leq S_{2n-1}\leq S_{2n}\leq S_2$
	- Satz 3.8: $\left(S_{2n}\right),\left(S_{2n-1}\right)$ konvergieren
	- $$\lim_{n\rightarrow\infty}S_{2n}-\lim_{n\rightarrow\infty}S_{2n-1}=\lim_{n\rightarrow\infty}\left(S_{2n}-S_{2n-1}\right)=\lim_{n\rightarrow\infty}a_{2n}=0$$
- Beispiel: Alternierende harmonische Reihen
  collapsed:: true
	- $$\sum_{k=1}^{\infty}\frac{\left(-1\right)^{k}}{k}=\sum_{k=1}^{\infty}\left(-1\right)^{k}\cdot\frac{1}{k}$$
	- konvergiert
	- -> $\sum_{k=1}^{\infty}\frac{\left(-1\right)^{k}}{k}=-\ln2$