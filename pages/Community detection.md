slide:: ![ns12](../assets/ns12.pdf)

- # Community
	- Perché studiare le comunità?
		- Scoprire l'organizzazione della rete
		- Identificare feature dei nodi
		- Classificare i nodi in base alla loro posizione nel cluster
		- Trovare link mancanti (?)
	- ### Alta coesione
		- Le comunità hanno molti link interni, per cui i loro nodi sono connessi assieme
	- ### Alta separazione
		- Le comunità sono connesse tra loro da pochi link
	- Per trovare comunità è necessario innanzitutto definirle **formalmente**
	- Ci sono molti modi per farlo, nessuno dei quali è considerato necessariamente il migliore
	- Si considerano sono le comunità non sovrapposte su grafi non diretti e non pesati, per cercare di capire la forza e i limiti di ogni approccio.
- ## Funzione di ottimizzazione del costo
	- È possibile definire una funzione costo che dica quanto sia buona una partizione di nodi e che faccia community detection semplicemente ottimizzando la funzione.
	- In questo caso, la funzione costo definisce il concetto di comunità, per cui ciò deve essere fatto attentamente.
	- ## Cut
		- Siano $N_1, N_2, \ldots, N_1$ una partizione nota in $q$ comunità. Ogni nodo del grafo appartiene a uno e solo uno di questi insiemi.
		- Si definisce il cut del grafo come il numero di archi che cadono tra nodi in comunità distinte.
		- $$\text{cut}(N_1, \ldots, N_q) = \frac12 \sum_{a=1}^q \sum_{i \in N_a} \sum_{b \neq a} \sum_{j \in N_b} A_{ij}$$
		- Questa definizione non è efficiente nel creare partizioni significative, dato che tende a isolare singoli nodi dal resto della rete.
		  collapsed:: true
			- ((647f3c89-521a-475f-830c-2a298f419189))
				- Partizione desiderabile, cut = 2
			- ((647f3cac-50eb-4078-8b70-04dc8b08c7dc))
				- cut = 1
	- ## Ratio cut
		- Si conta