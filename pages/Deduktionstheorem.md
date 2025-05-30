- $\Sigma,A\models B\Leftrightarrow\Sigma\cup\left\lbrace A\right\rbrace\models B$
-
- $\Sigma$ is *eine* Menge aussagenlogischer Formeln
- $\Sigma,A\models B$ gdw $\Sigma\models\left(A\rightarrow B\right)$
-
- **Modus-Ponens-Regel**
	- Es gilt $\left\lbrace A,A\rightarrow B\right\rbrace\models B$
		- insbesondere ist B eine Tautologie, wenn A, A->B Tautologien sind
	- Beweis
		- Gelte $\Sigma,A\models B$
		- zeige $\Sigma\models\left(A\rightarrow B\right)$
		- d.h. für alle Bewertungen $\varphi$, die $\Sigma$ erfüllen, muss A->B wahr sein
		- Sei $\varphi$ gegeben, sodass $\Sigma$ wahr ist
		- Fall 1: $\varphi\left(A\right)=1$
		- Fall 2: $\varphi\left(A\right)=0$
		- ---
		- Fall 1: $\varphi\left(A\right)=1$
			- Dann ist unter $\varphi$ nicht nur $\Sigma$ wahr, sondern auch $\Sigma\cup\left\lbrace A\right\rbrace$
			- Dadurch greift die Voraussetzung $\Sigma,A\models B$, wodurch $\varphi\left(B\right)=1$ gelten muss
			- Also $\varphi\left(A\rightarrow B\right)=1$
		- Fall 2: $\varphi\left(A\right)=0$
			- Dann ist auch $\varphi\left(A\rightarrow B\right)=1$
-