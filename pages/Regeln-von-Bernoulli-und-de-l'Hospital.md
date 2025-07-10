reference:: 13a

-
- Ziel: Grenzwerte vom Typ $\frac00,\frac{\pm\infty}{\pm\infty},1^{\infty},0^0$
	- $\left(1+\frac{1}{n}\right)^{n}\longrightarrow{}_{n\rightarrow\infty}e\rightsquigarrow\left(1+\frac{1}{x}\right)^{x}\longrightarrow{}_{x\rightarrow\infty}e$
	- Spezialfall: <Bild>
	- Idee: $\lim_{\xi\rightarrow x}\frac{f\left(\xi\right)}{f\left(\xi\right)}=\lim_{t\rightarrow0}\frac{f\left(x+t\right)}{g\left(x+t\right)}$
		- [[Taylor-Polynom]]:
			- $$f\left(x+t\right)=f\left(x\right)+tf^{\prime}\left(x\right)+t\rho\left(t\right)$$
				- mit $\rho\left(t\right)\longrightarrow{}_{t\rightarrow0}0$
			- $$g\left(x+t\right)=g\left(x\right)+tg^{\prime}\left(x\right)+t\sigma\left(t\right)$$
				- mit $\sigma\left(t\right)\longrightarrow{}_{t\rightarrow0}0$
		- $$\frac{f\left(x+t\right)}{g\left(x+t\right)}=\frac{f\left(x\right)+tf^{\prime}\left(x\right)+t\rho\left(t\right)}{g\left(x\right)+tg^{\prime}\left(x\right)+t\sigma\left(t\right)}$$
			- da $f\left(x\right)=0,g\left(x\right)=0$ (Spezialfall)
		- $$=\frac{f^{\prime}\left(x\right)+\rho\left(t\right)}{g^{\prime}\left(x\right)+\sigma\left(t\right)}\longrightarrow{}_{t\rightarrow0}\frac{f^{\prime}\left(x\right)}{g^{\prime}\left(x\right)}$$
		- Beispiel
			- $$\lim_{x\rightarrow0}\frac{\sin x}{x}=\lim_{x\rightarrow0}\frac{\frac{d}{dx}\sin x}{\frac{d}{dx}x}=\lim_{x\rightarrow0}\frac{\cos x}{1}=\frac11=1$$
-