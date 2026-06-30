reference:: 10.18

- für $f:\left\lbrack a.b\right\rbrack\rightarrow\mathbb{R}$ heißen $f_{+}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R},f_{-}:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ mit
  $$f_{+}\coloneqq\left\lbrace_{0,f\left(x\right)<0}^{f\left(x\right),f\left(x\right)\geq0}\right.,f_{-}\coloneqq\left\lbrace_{-f\left(x\right),f\left(x\right)<0}^{0,f\left(x\right)\geq0}\right.$$
  der Positiv- bzw. Negativteil von $f$
- für $x\in\left\lbrack a,b\right\rbrack:$
  $$f\left(x\right)=f_{+}\left(x\right)-f_{-}\left(x\right),\left|f\left(x\right)\right|=f_{+}\left(x\right)+f_{-}\left(x\right)$$
-
- # Integrierbarkeit von Positiv- und Negativteil
	- reference:: 10.19
	- $$f\in\mathbb{R}\left\lbrack a,b\right\rbrack\Rightarrow f_{+}\in\mathbb{R}\left\lbrack a,b\right\rbrack,f_{-}\in\mathbb{R}\left\lbrack a,b\right\rbrack$$
	- Beweis
	  collapsed:: true
		- sei $\varepsilon>0,\varphi,\psi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\leq\psi,\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$
		- $$\Rightarrow\varphi_{+}\leq f_{+}\leq\psi_{+},\psi_{-}\leq f_{-}\leq\varphi_{-}$$
		- Rechne
			- $$\int_{a}^{b}\left(\psi_{+}-\varphi_{+}\right)\leq\int_{a}^{b}\left(\psi-\varphi\right)<\varepsilon$$
			- $$\int_{a}^{b}\left(\varphi_{-}-\psi_{-}\right)\leq\int_{a}^{b}\left(-\varphi+\psi\right)<\varepsilon$$