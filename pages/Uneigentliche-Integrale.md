reference:: 13b

-
- Ziele:
	- $$\int_{a}^{\infty}\frac{1}{x}dx=???$$
-
- Definition: **unbestimmtes Integral**
	- reference:: 13.5
	- für $a\in\left\lbrack-\infty,\infty\right);b\in\left(-\infty,\infty\right\rbrack;c:a<c<b;f:\left(a,b\right)\rightarrow\mathbb{R}$, für die $\int_{\alpha}^{c}f\left(x\right)dx,\int_{c}^{\beta}f\left(x\right)dx$ für alle $\alpha,\beta:\alpha<\beta$ exisiteren
	- Wenn außerdem die Grenzwerte
	- $$\int_{a}^{c}f\left(x\right)dx\coloneqq\lim_{\alpha\downarrow a}\int_{\alpha}^{c}f\left(x\right)dx;\int_{c}^{b}f\left(x\right)dx\coloneqq\lim_{\beta\uparrow b}\int_{c}^{\beta}f\left(x\right)dx$$
	- existeren, dann heißt
	- $$\int_{a}^{b}f\left(x\right)dx\coloneqq\int_{a}^{c}f\left(x\right)dx\int_{c}^{b}f\left(x\right)dx$$
	- das uneigentliche Integral von f über (a,b)
-
- Beispiel
	- reference:: 13.6
	- logseq.order-list-type:: number
	  $$\int_0^1\frac{1}{\sqrt{x}}dx$$
		- $$=\lim_{\alpha\downarrow0}\int_{\alpha}^1\frac{1}{\sqrt{x}}dx=\lim_{\alpha\downarrow0}\left\lbrack2\cdot\sqrt{x}\right\rbrack_{\alpha}^1=\lim_{\alpha\downarrow0}\left(2-2\sqrt{\alpha}\right)=2$$
	- logseq.order-list-type:: number
	  $$\int_0^{\infty}\frac{1}{x^2}dx$$
		- $$=\lim_{\alpha\downarrow0}\int_{\alpha}^1\frac{dx}{x^2}+\lim_{\beta\uparrow\infty}\int_1^{\beta}\frac{dx}{x^2}=\lim_{\alpha\downarrow0}\left\lbrack-\frac{1}{x}\right\rbrack_{\alpha}^1+\lim_{\beta\uparrow\infty}\left\lbrack-\frac{1}{x}\right\rbrack_1^{\beta}$$
		- $$=\lim_{\alpha\downarrow0}\left(-1+\frac{1}{\alpha}\right)+\lim_{\beta\uparrow\infty}\left(-\frac{1}{\beta}+1\right)=\infty+1=\infty$$
		- => Integral existiert nicht (bzw. ist $\infty$)
-