public:: true
tags:: cna

- # Definizioni base
  id:: 6416dcb6-cf08-4329-8e18-c6e6ee5a5b17
	- Modello matematico che aiuta a rappresentare sistemi complessi in termini di nodi e connessioni.
	- È utile avere un linguaggio per comprendere gli **elementi base di una rete**.
	  Con un linguaggio, si è in grado di parlare propriamente di:
		- proprietà che caratterizzano la **struttura** e il **comportamento** delle reti
		- i ruoli delle reti nei **processi influenzati** che avvengono nelle strutture di rete
	- $G = (N, L)$
		- nodi $N = \{n_1, n_2, \ldots, n_l\} = \{1, 2, \ldots, l\}$
		- archi $L = \{(i, j) : i, j \in N\}$
	- I grafi possono essere pesati o non pesati, diretti o non diretti.
		- ((6422e82b-39c6-423f-933b-1bab177896d6))
	- ## Sottografo
		- grafo ottenuto selezionando un sottoinsieme dei nodi e degli archi tra quei nodi.
	- ## Cricca
		- un sottografo completo.
		- ((6422e8c1-c281-472a-88f2-8acd80803291))
- # Tipi di grafo
  id:: 6422f672-3d23-4979-9b1e-299afce67298
	- ## Grafo bipartito
	  id:: 64368a97-1853-46f2-946d-aba0b766a52e
		- ((6422f6a5-d4db-4b84-ada4-1624743597e3))
		- Due tipi di nodi
		- Esistono archi solo tra nodi di tipo opposto
		- > es: attore -> film
	- ## Rete multilayer
	  id:: 64368a97-78f5-40da-9106-66f02375b7b1
		- Una rete può avere più layer, ognuno con i suoi nodi e archi.
			- > es: reti di trasporto aereo di compagnie di volo distinte, ognuna con i suoi nodi e archi.
		- ### Link intralayer
			- collegano nodi nello stesso layer.
		- ### Link interlayer
			- collegano nodi in diversi layer.
		- ### Reti multiplex
			- gli insiemi dei nodi nei diversi layer sono identici
			- i link interlayer sono **accoppiamenti** che collegano lo stesso nodo in diversi layer
			- > es: i layer possono rappresentare diversi tipi di relazione in una rete sociale, come amicizia, legami familiari, colleghi, ecc.
	- ## Rete di reti
		- In generale, ogni layer di una rete può avere i suoi nodi e archi. Questa può essere chiamata una rete di reti (es: la rete elettrica e internet).
		- L'interazione tra reti in diversi layer sono catturate dai link interlayer.
		- > es: le stazioni energetiche comunicano tramite internet, i router sono attivati dalla rete elettrica.
		- **fallimento a cascata**
			- tipo di vulnerabilità imprevedibile che sorge nelle reti di reti, dato che un fallimento in una certa rete può causare problemi massicci in un'altra.
	- ## Rete temporale
	  id:: 64368a97-5d3e-4c20-8c62-6c42ceac80f6
		- Rete multiplex in cui i layer rappresentano collegamenti in diversi momenti (snapshot temporali), ad esempio retweet nel corso del tempo.
		- ((6422f7ff-54a9-473a-92ca-61838e57e96b))
	- ## Ipergrafo
	  id:: 64368a97-f886-49ab-ac70-c7ee24f76e37
		- Le interazioni possono coinvolgere più nodi contemporaneamente.
		- L'ipergrafo è rappresentato da una sequenza di iperarchi di dimensione maggiore o uguale a 2
		- > es: {(1,2), (1, 7, 8), (8, 9), (9, 10, 6), (3, 6, 5), (2, 3, 4)}
			- ((6422f88a-bb0b-4cc1-89d7-721690128b8f))
- # Proprietà locali
  id:: 6422f914-29f3-46f4-916c-35a9f825fdb7
	- ## Vicini
	  id:: 64368a97-1f6c-45e5-9071-f0d6ff26a06d
		- ((6422e876-bf06-40cf-a59b-34d694162589))
	- ## Grado
	  id:: 6422fb58-b14c-4f73-a8ce-c547d160c906
		- numero di collegamenti (o vicini)
			- $i \rightarrow N_i \quad k_i = |N_i|$
			- ((64230250-19c7-4f2f-9fc8-1c2960fa093f))
		- In grafi orientati:
		  card-last-interval:: 4
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2022-09-12T09:29:59.322Z
		  card-last-reviewed:: 2022-09-08T09:29:59.323Z
		  card-last-score:: 5
			- in-degree
				- $k_i^{\text{in}} = |P_i|$
			- out-degree
				- $k_i^{\text{out}} = |S_i|$
			- $k_i = k_i^{\text{in}} + k_i^{\text{out}}$
			- ((6423026c-827e-43b2-a8a9-50185c7bb278))
		- ### Singleton
			- nodo con grado 0
			- $N_i = \{\}, k_i = 0$
		- ### Hub
			- Nodi con grado alto
			- ((631cb57b-95f1-4f96-bde0-7c6e6c74e8e7))
		- ### Grado medio (grafi non orientati) #card
		  card-last-score:: 5
		  card-repeats:: 2
		  card-next-schedule:: 2022-12-23T09:02:07.725Z
		  card-last-interval:: 4
		  card-ease-factor:: 2.6
		  card-last-reviewed:: 2022-12-19T09:02:07.727Z
			- $$
			  \begin{split}
			  \begin{aligned}
			  k &= \frac{\sum_{i \in N} k_i}{N} \\
			  &= \frac{2L}{N} \\
			  &= \frac{dN(N-1)}{N} \\
			  &= d(N - 1) \\
			  \end{aligned}
			  \end{split}
			  \quad\quad
			  d = \frac{2L}{N(N-1)} \Rightarrow L = \frac{dN(N-1)}{2}
			  $$
		- ### Grado medio di una rete
			- $$\lang k \rang = \frac{\sum_i k_i}{N} = \frac{2L}{N}$$
		- ### Connessione tra grado medio e ((642308ed-6d6f-4c41-b709-e55f89808c85)) #card
		  card-last-score:: 3
		  card-repeats:: 1
		  card-next-schedule:: 2022-09-12T09:30:10.291Z
		  card-last-interval:: 4
		  card-ease-factor:: 2.36
		  card-last-reviewed:: 2022-09-08T09:30:10.292Z
			- $$d = \frac{< k >}{N-1} = \frac{< k >}{k_{\text{max}}}$$
	- ## Forza
	  id:: 64368a97-7c8d-411c-a1ab-d08880fe1e29
		- ((642302b7-b5c8-490d-9b50-a3a251e9b775))
		- grado pesato
			- $s_i = \sum_{j \in N_i}w_{ij}$
		- in-strength
			- $s_i^{\text{in}} = \sum_{j \in P_i}w_{ji}$
		- out-strength
			- $s_i^{\text{out}} = \sum_{j \in S_i}w_{ji}$
	- ## Densità e sparsità
	  id:: 64368a97-a071-42ad-9844-7d0ec1cf7814
		- ### Numero di nodi
			- $|N|$ o $N$
		- ### Numero di archi
			- $|L|$ o $L$
		- ### Massimo numero possibile di archi #card
		  card-last-score:: 5
		  card-repeats:: 1
		  card-next-schedule:: 2022-10-24T17:30:24.809Z
		  card-last-interval:: 4
		  card-ease-factor:: 2.6
		  card-last-reviewed:: 2022-10-20T17:30:24.810Z
			- $$L_{\text{max}} = \binom{N}{2} = \frac{N(N-1)}{2}$$
		- ### Densità #card
		  card-last-score:: 5
		  card-repeats:: 1
		  card-next-schedule:: 2022-10-24T17:30:25.948Z
		  card-last-interval:: 4
		  card-ease-factor:: 2.6
		  card-last-reviewed:: 2022-10-20T17:30:25.948Z
		  id:: 642308ed-6d6f-4c41-b709-e55f89808c85
			- $$d = \frac{L}{L_{\text{max}}} = \frac{2L}{N(N-1)}$$
		- ### Sparsità #card
		  card-last-interval:: -1
		  card-repeats:: 1
		  card-ease-factor:: 2.5
		  card-next-schedule:: 2023-05-15T22:00:00.000Z
		  card-last-reviewed:: 2023-05-15T01:42:39.786Z
		  card-last-score:: 1
			- Se la ((642308ed-6d6f-4c41-b709-e55f89808c85)) $d < 1$, il grafo è sparso.
				- Se $L$ è nell'ordine di $N$, il grafo è sparso.
				- Se $L$ è nell'ordine di $N^2$, il grafo è denso.
- # Proprietà globali #card
  id:: 64230819-c4a5-41cb-8c3c-1f5aa77033be
	- ## Cammini e distanze
	  id:: 64368a97-14dd-4a64-95fb-cc81a0328d14
		- ### Cammino
			- ${n_1, n_2, \ldots, n_l} \text{ tale che } \forall i : (n_i, n_{i+1}) \in L$
			  dove $l$ è la lunghezza.
			- #### Ciclo
				- cammino con nodi ripetuti
				- se non è un ciclo, è un **cammino semplice**
			- #### Cammino più breve
				- il cammino minimo tra due nodi.
				- nelle reti pesate, i pesi possono rappresentare le distanze tra due nodi adiacenti.
				- possono essere trovati con [[BFS]]
			- #### Distanza
				- lunghezza del cammino più breve tra due nodi.
				- un nodo singleton è considerato a distanza $\infty$ da ogni altro nodo.
		- ### Lunghezza media e diametro #card
		  card-last-score:: 5
		  card-repeats:: 1
		  card-next-schedule:: 2022-10-24T17:30:21.918Z
		  card-last-interval:: 4
		  card-ease-factor:: 2.6
		  card-last-reviewed:: 2022-10-20T17:30:21.919Z
			- #### Lunghezza media dei cammini
			  id:: 646328e9-959c-4cee-8058-d017e8806c35
				- $$< l > = \frac{\sum_{ij}l_{ij}}{N(N-1)}$$
			- #### Diametro
			  id:: 64368a97-9392-4dfc-8f6e-fc99ca2c919e
				- $$l_{\text{max}} = \max_{ij}l_{ij}$$
			- Se ci sono elementi disconnessi, APL e diametro sono indefiniti.
				- $< l > = \frac{\sum_{ij}l_{ij}}{N(N-1)} = \infty$
				- Trucco matematico:
					- $$< l > = \left(\frac{\sum_{ij}\frac{1}{l_{ij}}}{N(N-1)}\right)^{-1}$$
		- ### Small-world effect
		  id:: 64633030-d7ea-434e-ada5-456426e9b83b
			- Si può trovare una catena relativamente corta di conoscenti che collegano quasi qualunque coppia di individui nel pianeta.
			- In altre parole, la lunghezza media dei cammini è molto breve.
			- La lunghezza media dei cammini viene considerata breve quando cresce molto lentamente rispetto alla dimensione della rete, ad esempio logaritmicamente:
				- $< \mathcal{l}> \approx logN$
	- ## Connettività
	  id:: 64368a97-8099-48bf-b424-298fc228d1bb
		- ### Grafo connesso
			- esiste un arco tra ogni coppia di nodi.
		- ### Componente connessa
		  id:: 6bc08bd9-9b69-4966-80d2-012ab396bd72
			- sottografo connesso. Un grafo **non connesso** ha diverse componenti connesse.
		- ### Giant component
			- componente connessa più grande. Solitamente include una porzione sostanziale della rete
		- ### Singleton #card
		  card-last-interval:: -1
		  card-repeats:: 1
		  card-ease-factor:: 2.5
		  card-next-schedule:: 2023-05-15T22:00:00.000Z
		  card-last-reviewed:: 2023-05-15T01:43:01.126Z
		  card-last-score:: 1
			- compente connessa più piccola possibile
		- ## Grafi orientati
		  heading:: 2
			- ### Grafo debolmente connesso
				- esiste un cammino per ogni coppia di nodi in almeno una direzione
			- ### Grafo fortemente connesso #card
			  card-last-interval:: -1
			  card-repeats:: 1
			  card-ease-factor:: 2.5
			  card-next-schedule:: 2023-05-15T22:00:00.000Z
			  card-last-reviewed:: 2023-05-15T01:42:59.177Z
			  card-last-score:: 1
				- esiste un cammino per ogni coppia di nodi **a prescindere da quale nodo si scelga come partenza o destinazione.** Si può fare la stessa distinzione per le [componenti connesse.](((6bc08bd9-9b69-4966-80d2-012ab396bd72)))
				- #### In-component
					- l'insieme di nodi da cui si può **raggiungere** una componente fortemente connessa $S$, ma che non possono **essere raggiunti** da $S$
				- #### Out-component
					- l'insieme dei nodi che possono **essere raggiunti** da una componente fortemente connessa $S$, ma da cui non è possibile **raggiungere** $S$
	- ## Coefficiente di clustering
	  id:: 64625143-588e-4dc1-a991-4b27deea3a85
		- Nelle reti sociali è comune che una conoscenza in comune tra due persone porti i suoi due conoscenti a conoscersi.
		- ## Coefficiente di clustering di un nodo
			- La frazione di coppie dei vicini del nodo che sono connesse l'una all'altra.
			- Se $N_i$ è l'insieme dei vicini di $i$, e $\tau(i)$ è il numero di triangoli che coinvolgono $i$:
			- $$C(i) = \frac{\tau(i)}{\tau_{\text{max}}(i)} = \frac{\tau(i)}{\binom{k_i}{2}}
			  = \frac{2\tau(i)}{k_i(k_i - 1)} : |N_i| = k_i$$
			- Il coefficiente di clustering di un nodo A può anche essere definito come la *probabilità che due amici di A selezionati casualmente siano amici tra loro*.
		- ## Coefficiente di clustering di una rete
			- media dei coefficienti di clustering di tutti i nodi.
			- $$C = \frac{\sum_{i:k_i > 1} C(i)}{N_{k > 1}}$$
		- ## Coefficiente di clustering alto o basso
			- Osservando una rete per un certo periodo di tempo, si possono osservare diversi archi formarsi tramite la chiusura triadica, mentre altri si formano anche se i due endpoint non hanno vicini in comune.
			- **CC alto**
				- le reti sociali tendono ad avere coefficienti di clustering alti per la ((64625526-7abe-416b-8538-8f2d05123946)): ci conosciamo tramite amici in comune.
			- **CC basso**
				- se comparato con il CC in un grafo generato casualmente - un grafo casuale del genere deve avere lo stesso numero di nodi, e un uguale numero di archi rimescolati
					- tipico di reti bipartite e tree-like
			- Dati $G$, $G_R$ randomizzazione di $G$, il coefficiente di clustering è "alto" se:
				- $$CC(G) > > CC(G_R)$$
- # Rappresentazione di reti
  id:: 646275b2-aadf-4af3-a1bb-342376290004
	- ## Matrice di adiacenza
	  id:: 646275b2-7887-4bef-83fa-dbaf2a264cd5
		- Rappresentazione adatta per matrici compatte.
		- Memoria richiesta da una matrice di adiacenza è proporzionale a $N^2$.
		  id:: 64632463-ad06-42c4-9264-0668c5c2535e
		- ### Non orienatata
			- ((64230b35-a956-48b0-bcb8-ff6b79cb0e5f))
			-
			- $$
			  a_{ij} =
			  \begin{cases}
			  0 & \text{nessun arco} \\
			  1 & (i, j) \in L
			  \end{cases}
			  $$
			- $a_{ij} = a_{ji}$ (la matrice è simmetrica).
			- Il grado di un nodo può essere calcolato con:
			- $$k_i = \sum_j a_{ij} = \sum_j a_{ji}$$
		- ### Orientata
			- ((64230b84-bd6e-4fc3-969c-6e08959d2981))
			- \begin{aligned}
			  \begin{split}
			  k_i^{\text{out}} &= \sum_j a_{ij} \\
			  k_i^{\text{in}} &= \sum_j a_{ji} \\
			  \end{split}
			  \qquad
			  \begin{split}
			  s_i^{\text{out}} &= \sum_j w_{ij} \\
			  s_i^{\text{in}} &= \sum_j w_{ji} \\
			  \end{split}
			  \end{aligned}
	- ## Rappresentazioni sparse
		- ((64632463-ad06-42c4-9264-0668c5c2535e))
			- Nelle reti sparse, ciò è terribilmente inefficiente
				- la maggior parte dello spazio è sprecato salvando degli zeri (non-collegamenti)
				- Per reti molto grandi, le matrici di adiacenza non sono usabili.
		- ## Lista di adiacenza
		  id:: 646275b2-a596-4444-b231-f4aa39798f57
			- ((64230ba0-d361-4e1e-8d11-c35c5ade9ffd))
			- Nei grafi orientati, ogni arco è rappresentato due volte.
		- ## Lista di archi
		  id:: 646275b2-28f6-45b2-b967-282c42428b7e
			- ### Senza pesi
				- ((64230bbc-d085-4207-b4f2-64906fe84412))
			- ### Con pesi
				- ((64230bcc-1bb5-416d-874f-018c87c98472))
		- ## Grafi temporali
			- ((64230c55-31cc-4207-a209-c4a7fb5c37e6))