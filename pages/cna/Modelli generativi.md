tags:: cna
date:: [[2023-03-08]]
slide:: ![ns06](../assets/ns06.pdf)
ref:: ((64688dce-786d-4483-96aa-0f7794277d6c)), ((64688e49-92e6-499c-99fd-911bb70b2729)), ((64688f73-7e43-4586-be1a-2d62e5c79be1))

-
- # Caratteristiche delle reti nel mondo reale
	- Si vogliono studiare modelli casuali in modo da avere modo di osservare fenomeni che accadono in reti reali, quali:
		- ((632050e0-bd5f-4b71-9a56-f7ac016612e2))
		- ((64691261-efab-4f42-861d-9f03d240e6c5))
		- ((64691261-052f-498d-9deb-d401acccc910))
		- Eterogeneità
- # Modello di Erdos-Renyi #card
  id:: 646e2aea-4f90-47a5-83c2-0827e9bb2db1
  icon:: A
	- ✅ Distanza tra coppie di nodi è breve ( ((64633030-d7ea-434e-ada5-456426e9b83b)) )
	- ❌ Coefficiente di clustering medio molto più basso rispetto a reti reali della stessa dimensione e grado medio
	- ❌ I nodi hanno approssimativamente lo stesso grado, non ci sono hub
	- ❌ Non esiste struttura di comunità
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
  id:: 6474d86d-605b-4e46-bb17-7dc0190990f8
	- ✅ Le distanze tra coppie di nodi sono brevi ( ((64633030-d7ea-434e-ada5-456426e9b83b)) ), ereditato dal ((646e2aea-4f90-47a5-83c2-0827e9bb2db1))
	- ✅ È possibile usare qualunque distribuzione di gradi
	- ❌ Il coefficiente di clustering è molto più basso delle reti reali della stessa dimensione e grado medio
	- ❌ Non c'è struttura di comunità
	- ## Definizione
	  id:: 647b0223-70de-4a69-b566-83282359e171
		- Modello per costruire reti con una distribuzione di gradi predeterminata.
		- **[degree](((6462989a-ec74-4814-ba4f-745fd640511c))) sequence**
			- lista di $N$ numeri $k_1, k_2, \ldots, k_N$ dove $k_i$ è il grado del nodo $i$
		- **principio**
			- si sceglie il grado di ogni nodo
			- si piazza un numero di "pezzi" di arco su ogni nodo corrispondente al suo grado scelto
			- si vanno a collegare coppie di pezzi di arco a caso
		- ### Degree-preserving randomization
			- si generano versioni randomizzate di una data rete con la stessa sequenza di gradi usando il configuration model
			- è utile per vedere se specifiche proprietà della rete dipendono soltanto dalla distribuzione dei gradi
				- se la proprietà è mantenuta nella configurazione randomizzata, allora la distribuzione dei gradi è il fattore principale
		- [Versione casuale](((647b05ec-3199-41c1-a38d-9deed6ff9c3f)))
			- Assegna a ogni nodo una probabilità $p_i$
			- Genera archi indipendentemente con probabilità:
				- $$P(A_{ij} = 1) = p_i p_j$$
			- Il grado atteso di $i$ si legge (**la connettività non è garantita**)
				- $$\mathbb{E}[k_i] = \sum_{j \neq i} \mathbb{E}[A_{ij}] \approx p_i n \lang p \rang$$
	- ## Coefficiente di clustering
	  id:: 647b04ce-8cd3-4492-9c42-2bbf4933731b
		- Vicini di alto grado hanno maggiore probabilità di essere connessi, per cui l'eterogeneità migliora il clustering
		- La casualità tuttavia rende triangoli rari, specialmente in reti grandi.
			- ((647b0bde-4d0f-4f97-9ad4-ef60f9c15923))
- # Modello di Watts-Strogatz
  id:: 647b01a1-62ad-4621-800e-5a4bc84eebba
	- C'è un range di valori per la probabilità di riconfigurazione $p$ per cui:
		- ✅ distanze tra nodi sono brevi ( ((64633030-d7ea-434e-ada5-456426e9b83b)) ) e
		- ✅ coefficiente di clustering medio è alto
	- ❌ I nodi hanno approssimativamente lo stesso grado, non esistono hub
	- ❌ Non c'è struttura di comunità
	- ## Definizione
	  id:: 647b0f9f-5bfb-490e-bae9-4ba93b52bfa3
		- La casualità porta a diametri piccoli e coefficienti di clustering bassi
		- **Soluzione**: interpolare tra un lattice regolare (clustering alto) e rete casuale (small world property)
		- Un lattice ha:
			- ✅ Coefficiente di clustering alto
				- i nodi interni hanno $k = 6$ vicini, di cui sei coppie sono connesse.
				- $C = \frac{6}{(6 \cdot 5) / 2} = \frac{6}{15} = \frac25 = 0.4$
				- La maggior parte dei nodi sono interni, per cui il coefficiente di clustering  medio della rete è vicino a 0.4
			- ❌ Lunghezza media dei cammini più brevi lunga
				- Arrivare da un nodo a un altro può richiedere un grande numero di passi, che cresce rapidamente con la dimensione della rete
		- Alla base del modello c'è un lattice ad anello, formato da $N$ nodi e di grado $k$ pari.
			- Ogni link è ricollegato casualmente in base a una probabilità $p$.
			- Il numero atteso di link ricollegati è $pL = pNk/2$
			- !["Figure 5.1: A ring lattice with n=10 and k=4."](https://runestone.academy/ns/books/published/complex/_images/thinkcomplexity2007.png)
				- A ring lattice with n=10 and k=4.
		- ## Coefficiente di clustering e diametro
		  id:: 647c9827-815b-4e96-a802-90f2ccfb5c2d
			- In base al valore di $p$:
				- Se $p = 0$ nessun link viene ricollegato: nessun cambiamento
				- Per un range piccolo di valori di $p$ (vengono ricollegati pochi collegamenti):
					- coefficiente di clustering resta approssimativamente lo stesso
					- le distanze diminuiscono considerevolmente grazie a scorciatoie
				- Se $p = 1$, tutti i link vengono ricollegati: la rete diventa una rete casuale
		- ## Distribuzione dei gradi
		  id:: 647c3ae2-116d-411d-ac5c-5ace120cf885
			- Qual'è il grado dopo il reshuffling?
				- $$\bar{k} = k - k_\text{out} + k_\text{in}$$
				- \begin{aligned}
				  k_\text{out} &\sim \text{Bin}\left(\frac{k}2, p \right) \\
				  k_\text{in} &\sim \text{Bin}\left(\frac{(n-1)k}2, \frac{p}{n-1} \right) \\
				  \end{aligned}
			- $$\mathbb{E}[\bar{k}] = k$$
			- $$\text{Var}[\bar{k}] \approx \frac{k p(2 - p)}2$$
			- ((647c99cd-88c7-4523-84d4-ecb4d8922d4a))
				- La distribuzione dei gradi ha un picco dato che la maggior parte dei nodi ha lo stesso grado. **Non ci sono hub.**
				- Il modello di Watts-Strogatz fallisce nel riprodurre le distribuzioni di grado ampie osservate in molte reti reali.
- # Stochastic block model
	- Eredita la maggior parte delle sue proprietà dal modello di Erdos-Renyi
	- ✅ Distanze tra coppie di nodi brevi
	- ❌ I nodi hanno approssimativamente lo stesso grado, non ci sono hub.
		- ✅ Si può creare un mix con il configuration model e ottenere il *degree-corrected stochastic block model*
	- ✅ Crea una struttura di comunità
	- ## Definizione
		- Molte reti hanno una struttura di comunità: ci sono gruppi di nodi più strettamente connessi tra di loro che con gli altri.
		- Come generare una rete con comunità?
			- Si supponga di avere due comunità.
				- Ogni nodo ha etichetta $l = 1$ o $l = 2$.
				- Ogni arco è generato in modo casuale e indipendente con le seguenti probabilità:
					- $$P(A_{ij} = 1) = \begin{cases}
					  p_\text{in} & \text{se } l_i = l_j \\
					  p_\text{out} & \text{se } l_i \neq l_j
					  \end{cases}
					  $$
			- Impostando $p_\text{in} > p_\text{out}$ si ottiene la struttura di comunità desiderata.
			- Si può estendere questo ragionamento a più classi.
	-