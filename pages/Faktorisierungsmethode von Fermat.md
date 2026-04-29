reference:: Algebra 3.13

- Input: eine ungerade (zusammengesetze) Zahl $n\in\mathbb{N}$
- Output: Faktoren $a,b$ mit $a\cdot b=n$
-
- 1 $x\leftarrow\lceil\sqrt{n}\rceil$
- 2 $r\leftarrow x^2-n$
- 3 WHILE $\sqrt{r}\notin\mathbb{N}$ DO
	- 4 $r\leftarrow r+2x+1$
	- 5 $x\leftarrow x+1$
- 6 END WHILE
- 7 $y\leftarrow\sqrt{r}$
- 8 $a\leftarrow x+y$
- 9 $b\leftarrow x-y$
- 10 RETURN a,b
-