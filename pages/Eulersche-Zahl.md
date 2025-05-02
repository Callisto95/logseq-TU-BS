- Übung
	- reference:: 3.13
	- Sei $\left(e_{k}\right),\left(f_{k}\right)\in\mathbb{R}^{\mathbb{N}}$ gegeben
		- äquivalent zu $\left(e_{k}\right),\left(f_{k}\right)\subseteq\mathbb{R}$
	- mit $e_{k}:=\left(1+\frac{1}{k}\right)^{k},f_{k}:=\left(1+\frac{1}{k}\right)^{k+1}$
	- dabei $\left(e_{k}\right)$ steigt monoton
	  logseq.order-list-type:: number
	- $\left(f_{k}\right)$ sinkt monoton
	  logseq.order-list-type:: number
	- außerdem $\exists e\in\mathbb{R}:\lim_{k\rightarrow\infty}e_{k}=e=\lim_{k\rightarrow\infty}f_{k}$
	  logseq.order-list-type:: number
	- zu 1.) zZ: $\forall k\in\mathbb{N}_2:e_{k}\geq e_{k-1}$
		- $$\Leftrightarrow\frac{e_{k}}{e_{k-1}}\geq1$$
		- $$\frac{e_{k}}{e_{k-1}}=\frac{\left(1+\frac{1}{k}\right)^{k}}{\left(1+\frac{1}{k-1}\right)^{k-1}}\Leftarrow\left\lbrack1=\frac{k}{k}|\frac{k-1}{k-1}\right\rbrack\Rightarrow\frac{\left(\frac{k+1}{k}\right)^{k}}{\left(\frac{k}{k-1}\right)^{k-1}}=\frac{k+1}{k}\frac{\left(\frac{k+1}{k}\right)^{k-1}}{\left(\frac{k}{k-1}\right)^{k-1}}=\frac{k+1}{k}\left(\frac{k+1}{k}\cdot\frac{k-1}{k}\right)^{k-1}$$
		- $$=\frac{k+1}{k}\left(\frac{k^2-1}{k^2}\right)^{k-1}=\frac{k+1}{k}\left(1-\frac{1}{k^2}\right)^{k-1}$$
		- $$\Leftarrow\left\lbrack\text{Bernoulli}\right\rbrack\Rightarrow\frac{k+1}{k}\left(1-\frac{1}{k^2}\right)^{k-1}\geq\frac{k+1}{k}\left(1+\left(k-1\right)\cdot\frac{-1}{k^2}\right)=\frac{k+1}{k}-\frac{k+1}{k}\frac{k-1}{k^2}=\frac{k+1}{k}-\frac{k^2-1}{k^2}$$
		- $$=\frac{k+1}{k}-\frac{k^2-1}{k^3}=\frac{k^3+k^2-k^2+1}{k^3}=\frac{k^3+1}{k^3}\geq1$$
	- zu 2.) zZ: $\forall k\in\mathbb{N}_2:f_{k-1}\geq f_{k}$
		- $$\Leftrightarrow\frac{f_{k-1}}{f_{k}}\geq1$$
		- $$\frac{f_{k-1}}{f_{k}}=\frac{\left(1+\frac{1}{k-1}\right)^{k}}{\left(1+\frac{1}{k}\right)^{k+1}}=\frac{\left(\frac{k}{k-1}\right)^{k}}{\left(\frac{k+1}{k}\right)^{k+1}}=\frac{k}{k+1}\cdot\left(\frac{\frac{k}{k-1}}{\frac{k+1}{k}}\right)^{k}=\frac{k}{k-1}\cdot\left(\frac{k}{k-1}\cdot\frac{k}{k+1}\right)^{k}$$
		- $$\frac{k}{k+1}\cdot\left(\frac{k^2}{k^2-1}\right)^{k}=\frac{k}{k+1}\cdot\left(\frac{k^2-1+1}{k^2-1}\right)^{k}=\frac{k}{k+1}\cdot\left(1+\frac{1}{k^2-1}\right)^{k}$$
		- $$\Leftarrow\left\lbrack\text{Bernoulli}\right\rbrack\Rightarrow\frac{k}{k+1}\cdot\left(1+\frac{1}{k^2-1}\right)^{k}\geq\frac{k}{k+1}\left(1+k\cdot\frac{1}{k^2-1}\right)$$