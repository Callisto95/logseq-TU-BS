- **Vektorraum**
	- Körper K, V=(V,+) abelsche Gruppe
	- Abbildung: $K\times V\rightarrow V:(\alpha,v)\mapsto\alpha\cdot v$ (*multiplikation von Skalaren*)
		- $u,v\in V,\alpha$
		- $\alpha\cdot(u+v)=\alpha u+\alpha v$
-
- **Untervektorraum**
	- $U\subseteq V$
	- U besitzt Nullvektor
-
- **ineare Abbildungen**
	- Es seien V,W K-Vektorräume
	- $A\in L(V,W)$
	- Es gilt:
		- $L(V,W)\leq W^{V}=Map(V,W)$
		  logseq.order-list-type:: number
		- $(L(V),+,\circ)$ ist ein unitärer Ring, dessen Eins $I_{V}$ ist. Außerdem gilt $(L(V))^{\times}=Aut\ V$
		  logseq.order-list-type:: number
		- Für $U\leq V$ ist $A(U)\leq W$ ein Unterraum, insbesondere gilt dies für das Bild $Ran\ A=A(V)\leq W$
		  logseq.order-list-type:: number
			- Ran = Range = Menge der erreichbaren Vektoren
		- Für $T\leq W$ ist $A^{-1}(T)=\lbrace x\in V;A(x)\in T\rbrace\leq V$ ein Unterraum, insbesondere gilt $Ker\ A=A^{-1}\lbrace0\rbrace\leq V$
		  logseq.order-list-type:: number
			- Ker = Kern = Urbild des Vektorraums, welcher nur die 0 enthält
		- Die Lineare Abbildung A ist genau dann injecktiv, wenn $Ker\ A=\lbrace0\rbrace$ gilt
		  logseq.order-list-type:: number
-