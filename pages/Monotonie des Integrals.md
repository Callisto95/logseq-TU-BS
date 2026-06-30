reference:: 10.16

- sei $f,g\in\mathbb{R}\left\lbrack a,b\right\rbrack,f\leq g$
- Dann gilt
  $$\int_{a}^{b}f\leq\int_{a}^{b}g$$
- Beweis
  collapsed:: true
	- $$\int_{a}^{b}f=_{\ast}\int_{a}^{b}f=\sup\left\lbrace\int_{a}^{b}\varphi;\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq f\right\rbrace$$
	- $$\leq\sup\left\lbrace\int_{a}^{b}\varphi;\varphi\in\text{Trp}\left\lbrack a,b\right\rbrack,\varphi\leq g\right\rbrace$$
	- $$=_{\ast}\int_{a}^{b}g=\int_{a}^{b}g$$
-
- ## Korollar:
	- reference:: 10.17
	- für $f\in\mathbb{R}\left\lbrack a,b\right\rbrack$ gilt
	- $$\left|\int_{a}^{b}f\left(x\right)dx\right|\leq\left(b-a\right)\cdot\left\lbrack\sup_{x\in\left\lbrack a,b\right\rbrack}\left|f\left(x\right)\right|\right\rbrack_{\eqqcolon M}$$
	- Beweis
	  collapsed:: true
		- $$\left|\int_{a}^{b}f\left(x\right)dx\right|=\pm\int_{a}^{b}f\left(x\right)dx=\left\lbrack\int_{a}^{b}\left(\pm f\left(x\right)\right)dx\right\rbrack_{\geq M}$$
		- $$\leq\int_{a}^{b}Mdx=M\cdot\left(b-a\right)$$
-