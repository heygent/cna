tags:: cna

- # BFS
	- Uno degli algoritmi più efficienti per trovare la distanza. #.ol
		- Parti da un nodo sorgente (radice).
		- Visita l'intera ampiezza del grafo entro una certa distanza dalla sorgente, prima di spostarti a una profondità maggiore (più distante dalla radice)
		- Parti da ogni nodo per trovare tutte le coppie di cammini più brevi $(O(N^2))$
	- La BFS scopre le distanze verso i nodi uno strato alla volta.
	  Ogni strato è fatto di nodi che hanno un arco verso almeno un nodo nello strato precedente.
	- ((64231dcf-4412-43db-9ee6-b74f227616d7))
	- Ogni nodo ha un attributo che contiene la propria distanza $l$ dalla sorgente.
		- inizialmente $l = -1$ tranne $l_\text{source} = 0$.
	- Una coda FIFO contiene la frontiera, inizialmente la radice.
	- In output viene restituito un **albero dei cammini più brevi**, inizialmente contenente tutti i nodi e nessun arco.
	- Itera finché la frontiera non è vuota: #.ol
		- Rimuovi il nodo successivo $i$ dalla frontiera
		- Per ogni vicino/successore $j$ di $i$ con $l(j) = -1$: #.ol-nested
			- Accoda $j$ nella frontiera #.ol-nested
			- $l = l + 1$
			- Aggiungi il link $i \rightarrow j$ all'albero dei cammini più brevi