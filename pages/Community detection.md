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
	- In questo caso, la funzione costo definisce il cone