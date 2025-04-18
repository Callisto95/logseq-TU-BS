- **ungerichteter Graph**
	- ungerichteter Graph ist $G(V,E,\Psi)$
		- V,E sind endliche Mengen
		- V ist die Knotenmenge, |V| ist die Anzahl der Knoten (auch meist n)
		- E ist die Kantenmenge, |E| isy die Anzahl der Kanten (auch m)
		- $\Psi$ ist eine Funktion: $\Psi:E\rightarrow\lbrace X\subseteq V:1\leq|X|\leq2\rbrace$ (jede Kante enthält einen oder zwei Knoten [Schleife oder Verbindung])
	- Zwei Kanten ($e,e^{\prime}\in E$) sind parallel, wenn $\Psi(e)=\Psi(e^{\prime})$
	- EIne Kante ($e\in E$) ist eine Schleifen, wenn $|\Psi(e)|=1$
	-
	- ein Graph ohne parallele Kanten und Schleifen heißt **einfacher Graph**
		- $G=(V,E)$ mit $E(G)$ als Kantenmenge von G
		- $\lbrace v_{i},v_{j}\rbrace$ als Kante $e_{i,j}$ zwischen den Punkten $v_{i}$ und $v_{j}$
-
- **Nachbarschaft in Graphen**
	- Kante $e=\lbrace v,w\rbrace$ verbindet zwei Knoten $v$ und $w$. $v$ ist dann Nachbar von $w$. $v$ und $w$ sind *adjazent* (benachbart)
	- $v$ und $w$ sind jeweils *inzident* (zusammentreffend) mit $e$
-
- **Teilgraph**
	- $H=(V(H),E(H))$ eines Graphen $G=(V(G),E(G))$
	- $V(H)\subseteq V(G)$ und $E(H)\subseteq E(G)$
	- $H$ ist *aufspannend*, wenn $V(H)=V(G)$ gilt
		- H hat genau die selben Knoten wie G
-
- **Kantenfolge**
	- Kantenfolge $W$ in einem Graphen $G=(V,E)$ ist eine Folge $v_1,e_1,v_2,e_2,...,v_{k},e_{k},v_{k+1}$ mit $k\geq0,e_{i}=\lbrace v_{i},v_{i+1}\rbrace,v_1,...,v_{i}\in V$
	- Wiederholt sich *keine Kante* in einer Kantenfolge, dann ist die Kantenfolge ein **Weg**
	- Wiederholt sich *kein Knoten* in einer Kantenfolge, dann ist die Kantenfolge ein **Pfad**
-
- Definitionen
	- ein *geschlossener Weg* (**Tour**) kehrt am Ende zum Startknoten zurück
	- ein Kreis ist ein geschlossener Pfad
	- ein *Eulerweg* ist ein Weg, der alle Kanten eines Graphen verwendet
		- einen Eulerweg kann es nur geben, wenn es höchstens zwei Knoten mit ungeradem Grad gibt
		- eine *Eulertour* kehrt außerdem zum Startknoten zurück
	- ein *Hamiltonpfad* ist ein Pfad, der alle Knoten eines Graphen besucht
		- ein *Hamiltonkreis* (Hamiltontour) kehrt außerdem zum Startknoten zurück
	- ein Graph ist *zusammenhängend*, wenn es zwischen je zwei Knoten einen Weg gibt
	- der *Grad eines Knotens* $v$ ist die Anzahl der inzidenten Kanten: bezeichnet mit $\delta(v)$
	- *Schleife*: Kante mit nur einem Knoten
	- *Parallele Kanten*: Menge der Knoten von zwei (oder mehr) Kanten sind gleich
	-
	- **Wald**: Kreisfreier Graph
	- **Baum**: [[Zusammenhangskomponente]] in einem Wald (kreisfreier, zusammenhängender Graph)
	- **aufspannender Baum** (Spannbaum): Baum, welcher alle Knoten verbindet
	-