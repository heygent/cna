tags:: cna
date:: [[2023-03-08]]
slide:: ![ns06](../assets/ns06.pdf)
ref:: ((64688dce-786d-4483-96aa-0f7794277d6c)), ((64688e49-92e6-499c-99fd-911bb70b2729)), ((64688f73-7e43-4586-be1a-2d62e5c79be1))

-
- # Caratteristiche delle reti nel mondo reale
	- ((632050e0-bd5f-4b71-9a56-f7ac016612e2))
	- ((64691261-efab-4f42-861d-9f03d240e6c5))
	- ((64691261-052f-498d-9deb-d401acccc910))
- # Grafo casuale di Erdos-Renyi
  id:: 646e2aea-4f90-47a5-83c2-0827e9bb2db1
	- ## Sintesi
	  id:: 647afbed-6365-450a-93e2-1f076785a053
		- Distanza tra coppie di nodi è breve (small-world property) (buono)
		- Coefficiente di clustering medio molto più basso rispetto a reti reali della stessa dimensione e grado medio (male)
		- I nodi hanno approssimativamente lo stesso grado, non ci sono hub (male)
		- Non esiste struttura di comunità (male)
	- ## Definizione
	  id:: 647afc73-6c56-46ae-86ed-68a9eb874e71
		- Gilbert: $G(n, p)$
			- ogni coppia di nodi è connessa con probabilità $p$
		- Erdos-Renyi: $G(n,L)$
			- ci sono $L$ archi casualmente piazzati
		- ((646e5059-6e19-49ef-8012-3a7ed60bdf94))
		- $G(n,p)$ è equivalente a $G(n,L)$ se:
			- $$L \sim \text{Binomiale}\left(\frac{n(n-1)}{2}, p \right)$$
	- ## Algoritmo (Gilbert)
		- Parti da un grafo con $N$ nodi senza link
		- Per ogni coppia di nodi $i$ e $j$:
			- Genera un numero casuale $r$ tra 0 e 1
			- Se $r \le p$ crea l'arco $(i, j)$
	- ## TODO Transizione di fase (Percolation threshold)
	  id:: 646efb6f-975d-4540-be73-efe075b8fa3e
	- ## Distribuzione dei gradi
	  id:: 646f6b87-dcb3-453f-a8cb-b8b87442c6fe
		- La distribuzione del grado di un nodo è binomiale di parametri $p$, $N - 1$
		- Probabilità che il lancio di una moneta di probabilità $p$ risulti in $k$ teste in $N-1$ prove.
		- $$P(k) = \binom{N-1}{k} p^k (1-p)^{N-1-k}$$
		- Per $p$ piccolo ed $N$ grande la distribuzione binomiale approssima una normale
		- La maggior parte dei gradi sono centrati sul picco, per cui **la media è un buon descrittore della distribuzione**.
		- ### Grado medio
			- $\lang k \rang = (N-1) \cdot p = d$
		- ((6476078f-fdc6-4633-9480-db319311ed6e))
			- La distribuzione dei gradi è generalmente **molto diversa** rispetto alle reti reali.
	- ## Diametro
	  id:: 64760805-49ab-4d2d-83eb-9edfc0da761c
		- Quanti nodi posso raggiungere in media con $d$ passi?
		- Dato che tutti i nodi hanno approssimativamente lo stesso grado, si assume che abbiano lo stesso grado $k$.
			- $d = 1$: $k$ nodi
			- $d = 2$:  $k(k-1)$ nodi
			- in generale: $k(k-1)^{d-1}$
		- Se $k$ non è troppo piccolo, il numero totale di nodi entro una distanza $d$ da un dato nodo è approssimativamente:
			- $$N_d \sim k(k-1)^{d-1} \sim k^d$$
		- Quanti passi servono per coprire l'intera rete?
			- \begin{aligned}
			  N &\sim k^{d_\text{max}} \\
			  \log N &\sim d_\text{max} \log k \\
			  d_\text{max} &\sim \frac{log N}{log k}
			  \end{aligned}
			- **Il diametro della rete cresce come il logaritmo della dimensione della rete.**
			- Ad esempio, $N = 7.000.000.000, k = 150$
				- $d_\text{max} = 4.52$
	- ## Coefficiente di Clustering
	  id:: 647af7d1-43d5-40c2-b426-e2585c96c821
		- Il coefficiente di clustering di un nodo $i$ può essere interpretato come la probabilità che due vicini di $i$ siano connessi:
			- {{embed ((647af84d-79ee-4348-b2a6-e8911d7311c6))}}
		- Qual'è la probabilità che i due vicini di un nodo siano connessi?
			- Dato che i collegamenti sono piazzati indipendentemente l'uno dall'altro, è la probabilità $p$ che una coppia di nodi nel grafo sia connessa:
			- $$C_i = p = \frac{\lang k \rang}{N-1} \sim \frac{\lang k \rang}N$$
		- Dato che $\lang k \rang$ è solitamente piccolo, il coefficiente di clustering medio di reti casuali per valori realistici di $\lang k \rang$ ed $N$ è molto più piccolo rispetto a quello osservato in reti reali.
- # Configuration model
	- ## Definizione
		- Modello per costruire reti con una distribuzione di gradi predeterminata.
		- **degree sequence**
			- lista di $N$ numeri $k_1, k_2, \ldots, k_N$ dove $k_i$ è il grado del nodo $i$
		- **principio**
			- si sceglie il grado di ogni nodo
			- si piazzano "pezzi" di arco su ogni nodo
		- ((647b02e2-097e-494f-a080-38766a1bfd8a))
			-
- # Modello di Watts-Strogatz
	-