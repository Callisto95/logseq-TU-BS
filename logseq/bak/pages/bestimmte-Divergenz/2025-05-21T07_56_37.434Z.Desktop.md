- Wenn $\forall r>0:\exists n=n\left(r\right):\forall k\geq n:a_{k}>r$ gilt, schreibe $\lim_{a\rightarrow\infty}a_{k}=\infty$
- Wenn $\forall r>0:\exists n=n\left(r\right):\forall k\geq n:a_{k}<-r$ gilt, schreibe $\lim_{a\rightarrow\infty}a_{k}=-\infty$
-
- **Theorem: Bolzano-Weierstraß**
	- reference:: 3.23
	- Sei $\left(x_{k}\right)\subseteq\mathbb{R}$ eine beschränkte Folge
	- => $\left(x_{k}\right)$ besitzt eine konvergente Teilfolge
	- Beweis
	  collapsed:: true
		- Folge wird halbiert
		- in einer Hälfte sind unendlich Folgeglieder
		- betrachte diese Hälfte
		- wiederhole
		- ---
		- da $\left(x_{k}\right)$ beschränkt
		- => Intervall $I_0=\left\lbrack a_0,b_0\right\rbrack\subseteq\mathbb{R}$ mit $\forall k\in\mathbb{N}:x_{k}\in I_0$
		- Konstruiere rekursiv eine Intervallschachtelung $\left(I_{k}\right)$ mit $I_{k}=\left\lbrack a_{k},b_{k}\right\rbrack$ und eine Teilfolge $\left(x_{\tau_{k}}\right)$ mit
			- logseq.order-list-type:: number
			  $$\forall k\in\mathbb{N}:\text{diam}I_{k}=b_{k}-a_{k}=2^{-k}\left(b_0-a_0\right)$$
			- logseq.order-list-type:: number
			  $$\forall k\in\mathbb{N}:x_{\tau_{k}}\in I_{k}$$
		- Schritt
			- $I_0,...,I_{k}$ und $x_{\tau_{k}}\in I_{k}$ gegeben
			- Falls $L_{k}$ unendlich viele $x_{k}$ enthält, wähle $I_{k+1}:=L_{k}$
			- Sonst $I_{k+1}:=R_{k}$, da zwangsweise $R_{k}$ unendlich viele Folgeglieder hat
			- => $I_{k+1}$ enthält unendlich viele $x_{k}$
			- Wähle ein beliebigen $\tau_{k+1}\in\mathbb{N}:\tau_{k+1}>\tau_{k}$ und $x_{\tau_{k+1}}\in I_{k+1}$
			- Intervallschachtelungsprinzip: $a_{k}\leq x_{\tau_{k}}<b_{k}$
			- durch [[Sandwich-Kriterium]] $k\rightarrow\infty:\xi\leq?\leq\xi$, also $\lim_{k\rightarrow\infty}=\xi$
-