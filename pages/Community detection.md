tags:: cna
slide:: ![ns12](../assets/ns12.pdf), ![ns13](../assets/ns13.pdf), ![ns14](../assets/ns14.pdf)
ref:: ((647f4e7e-1970-4e54-868d-b71b13d6c98c))

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
		- Non efficiente nel creare partizioni significative, dato che tende a isolare singoli nodi dal resto della rete.
		  collapsed:: true
			- ((647f3c89-521a-475f-830c-2a298f419189))
				- Partizione desiderabile, cut = 2
			- ((647f3cac-50eb-4078-8b70-04dc8b08c7dc))
				- cut = 1
		- Risolvibile in tempo polinomiale
	- ## Ratio cut
		- Si conta il numero medio di connessioni che ogni nodo ha con nodi in altre comunità. Questo definisce il ratio cut:
			- $$\text{Rcut}(N_1, \ldots, N_q) = \frac12 \sum_{a=1}^q \frac1{|N_a|} \sum_{i \in N_a} \sum_{b \neq a} \sum_{j \in N_b} A_{ij}$$
		- Questa definizione è più efficace.
		  collapsed:: true
			- ((647f3d6c-ebfe-4878-943d-26ebc3d2303e))
				- rcut = $\frac12 \left[ \frac25 + \frac24 \right] = \frac9{20}$
			- ((647f3dbe-9bf2-4ece-b5f9-a46f15a3e096))
				- rcut = $\frac12 \left[ \frac18 + \frac11\right] = \frac9{16}$
		- NP-completo
			- nel caso peggiore, è necessario provare tutte le possibili configurazioni ($q^n$) e vedere quale sia la migliore.
		- Favorisce configurazioni in cui le comunità hanno approssimativamente la stessa dimensione.
	- ## ((647f5020-f73c-49a6-ab9b-ffe2e13466bb))
	- ## ((647f50b7-c4cf-46db-b61b-2282aa08cebe))
- #
- {{video https://www.youtube.com/watch?v=cxTmmasBiC8&t=450s}}