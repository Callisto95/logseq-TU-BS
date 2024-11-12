alias:: Zusammenhangskomponente

-
- **s-t-Weg**
	- Gegeben: Graph G=(V,E), Startknoten s, Endknoten t (start, target ?)
	- Gesucht: Weg von s nach t
-
- **Zusammenhangskomponente**
	- Gegeben: Graph G=(V,E), Startknoten s
	- Gesucht: Alle von s erreichbaren Knoten
-
- Wenn ein Weg zwischen zwei Knoten existiert, dann existiert auch ein Pfad zwischen diesen
	- Eliminierung von Kreisen (Knoten wird mehrmals besucht)
	- -> Entspricht auch den kürzesten Weg zwischen s und t
		- Kreisfreie Menge von Kanten, die den kürzesten Weg sichert
-
-