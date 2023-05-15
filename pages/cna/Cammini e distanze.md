tags:: cna

- cammino
  id:: 6319fcf7-097e-42c0-a5aa-dac7b51182c6
	- ${n_1, n_2, \ldots, n_l} \text{ tale che } \forall i : (n_i, n_{i+1}) \in L$
	  dove $l$ è la lunghezza.
	- **ciclo**
		- cammino con nodi ripetuti
		- se non è un ciclo, è un **cammino semplice**
- cammino più breve
	- il cammino minimo tra due nodi.
	- nelle reti pesate, i pesi possono rappresentare le distanze tra due nodi adiacenti.
- distanza
  id:: 6319be1d-d038-4df4-ae99-dc9ec8844242
	- lunghezza del cammino più breve tra due nodi.
	- un nodo singleton è considerato a distanza $\infty$ da ogni altro nodo.
- ## APL e diametro #card
  card-last-interval:: 4
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2022-10-24T17:30:21.918Z
  card-last-reviewed:: 2022-10-20T17:30:21.919Z
  card-last-score:: 5
	- Average Path Length
		- $$< l > = \frac{\sum_{ij}l_{ij}}{N(N-1)}$$
	- diametro
		- $$l_{\text{max}} = max_{ij}l_{ij}$$
	- Se ci sono elementi disconnessi, APL e diametro sono indefiniti.
		- $< l > = \frac{\sum_{ij}l_{ij}}{N(N-1)} = \infty$
		- Trucco matematico:
			- $$< l > = \left(\frac{\sum_{ij}\frac{1}{l_{ij}}}{N(N-1)}\right)^{-1}$$
	- La APL è corta quando **cresce molto lentamente** rispetto alla dimensione della rete, ad esempio logaritmicamente:
		- $< \mathcal{l}> \approx logN$