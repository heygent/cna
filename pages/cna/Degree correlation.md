tags:: cna

- "Omofilia per grado"
- Considerando un solo nodo, questo può avere diverse caratteristiche e tratti, ma ci sono anche caratteristiche strutturali per quel nodo, ovvero il suo numero di connessioni o ((631a06f3-fc3f-44e7-b3cf-07abfcab7cda))
- Se stiamo cercando l'omofilia, possiamo dire di **cercare la correlazione tra la presenza di un link tra due nodi e le loro similarità**
- **Hub**
  id:: 631cb57b-95f1-4f96-bde0-7c6e6c74e8e7
	- nodo con più probabilità di avere un ((6422fb58-b14c-4f73-a8ce-c547d160c906)) più alto rispetto agli altri
	- **positive degree correlation**
		- è più probabile che gli hub siano connessi tra di loro
- **reti assortative**
	- ((631cb6ad-94b9-4ccb-b446-c7848a2813a7))
	- hanno una struttura **core-periphery** con hub nel nucleo
	- es. reti sociali
- **reti disassortative**
	- ((631cb6d3-1221-43ae-b509-7156638eeab3))
	- hanno una struttura **hub-and-spoke**
	- in questo caso si ha **negative degree correlation**
	- es. internet
- Questa misura permette di caratterizzare la rete più ad alto livello.
- ## Degree correlation function
  id:: 631cb760-87bb-497c-94e9-c668dc397c7c
	- metodo per computare l'assortatività
	- è la correlazione tra
		- grado di un nodo
		- grado medio dei vicini di nodi con quel grado
	- Si calcola la media dei gradi dei vicini di $i$:
		- $$k_{nn}(i) = \frac{1}{k_i} \sum_j a_{ij} k_j$$
	- Con un leggero _**abuso di notazione**_, definiamo la funzione di correlazione del grado come la media di tutti i $k_{nn}(k_i)$ per tutti i nodi il cui grado è $k$:
		- $$k_{nn}(k) = \langle k_{nn}(i) \rangle_{i:k_i = k}$$
	- Per osservare visivamente l'assortatività di rete, si traccia il grafico:
		- $$(k, k_{nn}(k))$$
- ## Assortatività in una rete casuale
	- **rete neutrale**
		- non c'è correlazione tra il grado di un nodo e la media di grado dei vicini
	- È possibile dimostrare che in una rete neutrale fare il grafico di $k_{nn}(k)$ risulta in una linea orizzontale. Più precisamente:
		- $$k_{nn}(k) = \frac{\langle k^2 \rangle}{\langle k \rangle}$$
	- ((631cbf27-94d9-41de-8982-94f655e881a4))
	- ((631cbf3e-8d8c-4b36-97fd-ba5e032b510c))