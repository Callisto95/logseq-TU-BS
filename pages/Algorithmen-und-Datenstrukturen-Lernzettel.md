- Ein Algorithmus hat die Eigenschaften:
	- **Finitheit**: eindeutige Beschreibbarkeit des Algorithmuses in endlichem Text
	- **Ausführbarkeit**: Jeder Schritt des Algorithmuses muss auführbar sein
	- **Dynamische Finitheit**: Der Algorithmus muss nur endlich viel Speicherplatz benötigen
	- **Terminierung**: Der Algorithmus muss endliche viele Schritte haben
	- Dazu kommen auch
	- **Determinitheit**: Gleiche Eingaben liefern gleiche Ergebnisse
	- **Determinismus**: Alle Schritte sind festgelegt
	- **Randomisierter Algorithmus**: Determinitheit und Determinismus sind nicht bestimmt, es können zufällige Ergebnisse auftreten
-
- **Graphen**
	- Kante ist eine Menge aus zwei Knoten ($e=\left\lbrace v_1,v_2\right\rbrace$)
	  collapsed:: true
		- $v_1,v_2$ können sowohl verschiedene als auch unterschiedliche Knoten sein
		- wenn $v_1=v_2$ dann ist die Kante eine Schleife
	- *ungerichteter Graph*
		- $g=\left(V,E,\Psi\right)$
		- V, E endliche Mengen
		  collapsed:: true
			- V = vertices = Knotenmenge
			- E = edges = Kantenmenge
		- $\Psi:E\rightarrow\left\lbrace X\subseteq V|1\leq\left|X\right|\leq2\right\rbrace$
		  collapsed:: true
			- jede Kante enthält ein oder zwei Knoten (Schleife bzw. "gewöhnliche" Kante)
		- *parallele Kanten*: $e=e^{\prime}$ gdw $\Psi\left(e\right)=\Psi\left(e^{\prime}\right)$
		- eine Kante ist eine Schleife, falls $\left|\Psi\left(e\right)\right|=1$
		- *einfacher Graph*:
		  collapsed:: true
			- Graph ohne parallele Kanten
			- $G=\left(V,E\right)$ mit $E\left(G\right)$ als Kantenmenge von G
		-