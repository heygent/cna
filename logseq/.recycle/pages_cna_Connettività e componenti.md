tags:: cna

- **grafo connesso**
	- esiste un ((6319fcf7-097e-42c0-a5aa-dac7b51182c6)) tra ogni coppia di nodi.
- **componente connessa**
  id:: 6319c061-a46b-4578-bfee-b020da3db643
	- sottografo connesso. Un grafo **non connesso** ha diverse componenti connesse.
- **giant component**
  id:: 6319c11b-bddf-4fbb-bf24-9689c9e2f021
	- componente connessa più grande. Solitamente include una porzione sostanziale della rete
- **singleton**
	- compente connessa più piccola possibile
- ## Grafi orientati
	- **grafo debolmente connesso**
		- esiste un cammino per ogni coppia di nodi in almeno una direzione
	- **grafo fortemente connesso**
		- esiste un cammino per ogni coppia di nodi **a prescindere da quale nodo si scelga come partenza o destinazione.** Si può fare la stessa distinzione per le [componenti connesse.](((6319c061-a46b-4578-bfee-b020da3db643)))
		- in-component
			- l'insieme di nodi da cui si può **raggiungere** una componente fortemente connessa $S$, ma che non possono **essere raggiunti** da $S$
		- out-component
			- l'insieme dei nodi che possono **essere raggiunti** da una componente fortemente connessa $S$, ma da cui non è possibile **raggiungere** $S$