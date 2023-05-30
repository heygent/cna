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
		- $$P(k) = \left(\binom{N-1}$$
		-
		-
		- ((646f6c44-ee7a-4d35-8087-c11183dc27eb))
- # Configuration model
	- Modello per costruire reti con una distribuzione di gradi predefinita.
	-