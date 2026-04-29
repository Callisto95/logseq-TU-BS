reference:: 3.44

- reference:: Algebra 3.5
- sei $a\in\mathbb{Z},p\in\mathbb{P}$, dann gilt
  $$a^{p}\equiv a\bmod p$$
-
- wenn auch $p\nmid a$ gilt (also $\text{ggT}\left(n,p\right)=1$), dann
  id:: 69e09149-d0af-439d-ad5d-f07ddbe0cf2d
  $$a^{p-1}\equiv1\bmod p$$
	- (auch $n^{p-1}\%p=1$)
-
- Bemerkung
	- ![image.png](../assets/image_1737034353137_0.png){:height 167, :width 771}
-
- ## Fermat Test
-
- ## r-facher Fermat Test
  id:: 69f1d91c-382f-42cc-b6fb-54b7dad1eafb
	- Sei $N$ eine zusammengesetze Zahl, welche keine [[Carmichael Zahl]] ist. Dann gilt für zufällige Basen (unabhängig gewählt) $a_1,...,a_{r}\in\mathbb{Z}_{N}^{\times}$
		- $$P\left(a_{i}^{N-1}\equiv1\bmod N:i\in\left\lbrack1,r\right\rbrack\right)\leq2^{-r}$$
		- Die Wahrscheinlichkeit zu allen Basen $a_{i}$ Pseudoprim zu sein, ist für nicht-Carmichael Zahlen höchstens $2^{-r}$
-