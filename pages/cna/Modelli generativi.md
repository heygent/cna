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
	- ## Transizione di fase (Percolation threshold)
		- {{video https://youtu.be/VC43S6Thwg0?t=423}}
			- {{youtube-timestamp 423}} Emergence of the Giant Component
	- ## Distribuzione dei gradi
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
		- Numero totale di nodi entro una distanza $d$ da un dato nodo
		- ((647af7ad-cb59-4df4-ad09-5e80c8261c78))
		- ((647af7bd-c14a-436f-a9d1-44f14f106d9b))
	- ## Coefficiente di Clustering
		- Il coefficiente di clustering di un nodo $i$ può essere interpretato come la probabilità che due vicini di $i$ siano connessi:
			- {{embed ((647af84d-79ee-4348-b2a6-e8911d7311c6))}}
		- Qual'è la probabilità che i due vicini di un nodo siano connessi?
			- Dato che i collegamenti sono piazzati indipendentemente l'uno dall'altro, è la probabilità $p$ che una coppia di nodi nel grafo sia connessa:
			- $$C_i = p = \frac{\lang k \rang}{N-1} \sim \frac{\lang k \rang}N$$
		- Dato che $\lang k \rang$ è solitamente piccolo, il coefficiente di clustering medio di reti casuali per valori realistici di $\lang k \rang$ ed $N$ è molto più piccolo rispetto a quello osservato in reti reali.
- # Configuration model
	- Modello per costruire reti con una distribuzione di gradi predefinita.
	-