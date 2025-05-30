- Seien $\left(a_{k}\right),\left(b_{k}\right),\left(c_{k}\right)\subseteq\mathbb{R}$ mit $\forall k\in\mathbb{N}:a_{k}\leq b_{k}\leq c_{k}$
- Wenn außerdem $\left(a_{k}\right),\left(c_{k}\right)$ beide Konvergieren und ihre Grenzwerte übereinstimmen $\lim_{k\rightarrow\infty}a_{k}=\lim_{k\rightarrow\infty}c_{k}\eqqcolon b$
- dann gilt $\lim_{k\rightarrow\infty}b_{k}=b$
- Beweis
	- Sei $\varepsilon>0$
	- Es gibt Schwellenindezies $n_{a},n_{c}\in\mathbb{N}$ mit $\forall k\geq n_{a}:a_{k}\in\mathbb{B}_{\varepsilon}\left(b\right)$ (auch für $n_{c}$)
	- sei $n\coloneqq \max\left\lbrace n_{a},n_{c}\right\rbrace$
	- Wegen $\mathbb{B}_{\varepsilon}\left(b\right)=\left(b-\varepsilon,b+\varepsilon\right)$ gilt $k\geq n:b-\varepsilon<a_{k}\leq b_{k}\leq c_{k}<b+\varepsilon$
	- Kurz: $\forall k\geq n:b_{k}\in\mathbb{B}_{\varepsilon}\left(b\right)$