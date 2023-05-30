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
		- $\lang k \rang = (N-1) \cdot p = d$
		- ((6476078f-fdc6-4633-9480-db319311ed6e))
			- La distribuzione dei gradi è generalmente **molto diversa** rispetto alle reti reali.
	- ## Diametro
		- Quanti nodi ci sono in media a $d$ passi da un qualunque nodo?
		- > Question: what is the diameter of an erdos-renyi graph?
		  > The diameter of an Erdos-Renyi graph is given by the smallest value of ℓ such that P(dij > ℓ) is zero, and it is usually found to be relatively small and should scale logarithmically with n just as the average distance does (Newman2010 pages 434-435, Newman2010 pages 255-256). In the limit of large n, the diameter increases only slowly with n, as ln n, making it relatively small in large random graphs. The expression for the diameter is given by ℓ = ln a ln c + lim ϵ→0 (1 + ϵ) ln n, where A is a constant (Newman2010 pages 434-435). The logarithmic dependence of the diameter on n offers some explanation of the small-world effect. However, the diameter is generally a less useful measure of real-world network behavior than mean distance, since it only measures the distance between one specific pair of vertices at the extreme end of the distribution of distances (Newman2010 pages 255-256).
		  > Exercise 6 in Dall2023f pages 1-15 asks to find the diameter of a given graph, which can be calculated using the formula mentioned above. However, it is important to note that the diameter of a graph is not always smaller than the number of nodes, as Exercise 12 in Dall2023f pages 1-15 asks if the diameter of a graph is always smaller than the number of nodes. I cannot provide a definitive answer to this question without additional information.
			- > References
			- 1. (Newman2010): Newman, M. E. J. Networks: An Introduction. Oxford University Press, 2010.
			- 2. (Dall2023f): Dall'Amico, Lorenzo. "Lecture 27.ns19: Exercises." Complex Networks Analysis and Visualization, NetSci, University of Torino, email: lorenzo.dallamico@unito.it, 29 May 2023.
		-
- # Configuration model
	- Modello per costruire reti con una distribuzione di gradi predefinita.
	-