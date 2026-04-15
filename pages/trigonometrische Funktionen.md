- Satz: **Additionstheoreme für trigonometrische Funktionen**
	- reference:: 6.13
	- siehe auch: 6.10 (Skript)
	- für $z,w\in\mathbb{C}_{}$ gilt
	- logseq.order-list-type:: number
	  $$\cos\left(z+w\right)=\cos z\cdot\cos w-\sin z\cdot\sin w$$
	- logseq.order-list-type:: number
	  $$\sin\left(z+w\right)=\sin z\cdot\cos w+\cos z\cdot\sin w$$
	- Beweis
		- $\cos\left(z+w\right)$
		  logseq.order-list-type:: number
			- $$2\cdot\cos\left(z+w\right)=e^{i\left(z+w\right)}+e^{-i\left(z+w\right)}=e^{iz}\cdot e^{iw}+e^{-iz}\cdot e^{-iw}$$
			- $$=\left\lbrack\text{Euler}\right\rbrack=\left(\cos z+i\sin z\right)\cdot\left(\cos w+i\sin w\right)+\left(\cos\left(-z\right)+i\sin\left(-z\right)\right)\cdot\left(\cos\left(-w\right)+i\sin\left(-w\right)\right)$$
			- durch Potenzreihe: $\cos\left(-z\right)=\cos z,\sin\left(-z\right)=-\sin z$
			- $$=\cos z\cdot\cos w-\sin z\cdot\sin w+i\sin z\cdot\cos w+i\cos z\cdot\sin w+\cos z\cdot\cos w-\sin z\cdot\sin w-i\sin z\cdot\cos w-i\cos z\cdot\sin w$$
			- $$=2\cos z\cdot\cos w-2\sin z\cdot\sin w=\sim\cos z\cdot\cos w-\sin z\cdot\sin w$$
		- analog
		  logseq.order-list-type:: number
-
- Approximation für $x\approx0:$
	- $$\cos x=\sum_{k=0}^{\infty}\left(-1\right)^{k}\frac{x^{2k}}{\left(2k\right)!}=1-\frac{x^2}{2!}+r\left(x\right)$$
	- $$\sin x=\sum_{k=0}^{\infty}\left(-1\right)^{k}\frac{x^{2k+1}}{\left(2k+1\right)!}=x-\frac{x^3}{3!}+p\left(x\right)$$
	- dabei $r\left(x\right),p\left(x\right)$ klein für $x\approx0$
	- $$\tan x\coloneqq\frac{\sin x}{\cos x},\cot x\coloneqq\frac{\cos x}{\sin x}$$
-
- [[hyperbolische-Funktionen]]