reference:: 10.23

-
- sei $w:\left\lbrack a,b\right\rbrack\rightarrow\left\lbrack0,\infty\right)$ eine integrierbare "Gerichtsfunktion"
- => zu jeder stetigen Funktion $f:\left\lbrack a,b\right\rbrack\rightarrow\mathbb{R}$ gibt es eine Zwischenstelle $\xi\in\left\lbrack a,b\right\rbrack$ mit
	- $$\int_{a}^{b}f\left(x\right)w\left(x\right)dx=f\left(\xi\right)\cdot\int_{a}^{b}w\left(x\right)dx$$
- Beweis
  collapsed:: true
	- $$s\coloneqq\inf_{x\in\left\lbrack a,b\right\rbrack}f\left(x\right),t\coloneqq\sup_{x\in\left\lbrack a,b\right\rbrack}f\left(x\right)$$
	- $$\Rightarrow\forall x\in\left\lbrack a,b\right\rbrack:s\cdot w\left(x\right)\leq f\left(x\right)\cdot w\left(x\right)\leq t\cdot w\left(x\right)$$
	- $$\int_{a}^{b}\text{monoton}\Rightarrow s\cdot\int_{a}^{b}w\left(x\right)dx\leq\int_{a}^{b}f\left(x\right)w\left(x\right)dx\leq t\cdot\int_{a}^{b}w\left(x\right)dx$$
	- $$\Rightarrow\exists y\in\left\lbrack s,t\right\rbrack:\int_{a}^{b}f\left(x\right)w\left(x\right)dx=y\cdot\int_{a}^{b}w\left(x\right)dx$$
	- f stetig => $\exists\sigma,\tau\in\left\lbrack a,b\right\rbrack$ mit $f\left(\sigma\right)=s,f\left(\tau\right)=t$
	- ZWS => $\exists\xi\in\left(\sigma,\tau\right):y=f\left(\xi\right)$
-