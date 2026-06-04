# Kreisfunktionen
	- $$\sin:\mathbb{C}_{}\rightarrow\mathbb{C}_{},\space\space\space\cos:\mathbb{C}_{}\rightarrow\mathbb{C}_{}$$
		- $$\sin z\coloneqq\frac{1}{2i}\left(e^{iz}-e^{-iz}\right)$$
		- $$\cos\coloneqq\frac12\left(e^{iz}+e^{-iz}\right)$$
		- $$c=a+ib:a=\frac12\left(c+\overline{c}\right),b=\frac{1}{2i}\left(c-\overline{c}\right)$$
	- $$\tan z\coloneqq\frac{\sin z}{\cos z},\cot z\coloneqq\frac{\cos z}{\sin z}$$
	- Beweis
		- Kosinus
			- $$\cos z=\frac12\left(e^{iz}+e^{-iz}\right)$$
			- $$=\frac12\sum_{n=0}^{\infty}\frac{\left(iz\right)^{n}}{n!}+\frac12\sum_{n=0}^{\infty}\frac{\left(-iz\right)^{n}}{n!}$$
			- $$=\frac12\sum_{n=0}^{\infty}\frac{1+\left(-1\right)^{n}}{n!}i^{n}z^{n}$$
			- $$=\left\lbrack n=2k\right\rbrack=\sum_{k=0}^{\infty}\frac{i^{2k}}{\left(2k\right)!}z^{2k}$$
			- $$=\left\lbrack i^2=-1\right\rbrack=\sum_{k=0}^{\infty}\frac{\left(-1\right)^{k}}{\left(2k\right)!}z^{2k}$$
			- $$=\sum_{k=0}^{\infty}a_{n}z^{n}$$
			- $$a_{n}=\left\lbrace_{0,\text{ sonst}}^{\frac{\left(-1\right)^{k}}{\left(2k\right)!},n=2k}\right.$$
			- Konvergenzradius:
			- $$r=\left(\operatorname*{\mathrm{limsup}}_{k\rightarrow\infty}\sqrt[n]{\left|a_{n}\right|}\right)^{-1}=\left(\lim_{k\rightarrow\infty}\sqrt[2k]{\frac{1}{\left(2k\right)!}}\right)^{-1}=\infty$$
		- Sinus
			- $$\sin z=\frac{1}{2i}\left(e^{iz}-e^{-iz}\right)$$
			- $$=\frac{1}{2i}\left(\sum_{n=0}^{\infty}\frac{\left(iz\right)^{n}}{n!}-\sum_{n=0}^{\infty}\frac{\left(-iz\right)^{n}}{n!}\right)$$
			- $$=\frac{1}{2i}\sum_{n=0}^{\infty}\frac{1-\left(-1\right)^{n}}{n!}i^{n}z^{n}$$
			-
-
- # Additionstheoreme für trigonometrische Funktionen
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
- [[hyperbolische Funktionen]]
-