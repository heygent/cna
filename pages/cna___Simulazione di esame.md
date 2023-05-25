- ![Testo](../assets/cna_exam_simulation_may_2022.pdf)
- # Domande #.ol
	- Consider the [adjacency matrix](((646275b2-7887-4bef-83fa-dbaf2a264cd5))):
	  \begin{bmatrix}
	  0 & 2 & 1 & 0 \\
	  1 & 0 & 0 & 0 \\
	  1 & 0 & 0 & 0 \\
	  0 & 0 & 3 & 0 \\
	  \end{bmatrix}
		- Draw the graph
		- What type of graph is this?
		- What can you tell about the graph [connectivity](((64368a97-8099-48bf-b424-298fc228d1bb)))?
		- What is the in-out [degree](((6422fb58-b14c-4f73-a8ce-c547d160c906))) of each node?
		- Write the [strength](((64368a97-7c8d-411c-a1ab-d08880fe1e29))) and degree of each node.
	-
	- Consider an [ER random graph](((646e2aea-4f90-47a5-83c2-0827e9bb2db1))) with $n$ nodes and connecting probability equal to $p$. What is the expected [clustering coefficient](((64625143-588e-4dc1-a991-4b27deea3a85)))? How does this result relate to the clustering coefficient observed in real-world networks?
	-
	- How many edges are there in a Barabasi-Albert network with 1000 nodes and $m = 5$?
	-
	- Consider a Cayley tree as the one shown in the picture in which each node has $k$ neighbours (called offspring). Starting from a central node, we build the tree forming $l$ offspring levels.
	  ((646e2d78-304c-4db7-8df6-989c39dc75a2))
		- What is the number of nodes as a function of $l$ and $k$?
		- What is the [diameter](((64368a97-9392-4dfc-8f6e-fc99ca2c919e))) of this graph?
		- What property of real world graphs is well captured by this model?
	-
	- Consider the following graph. What is its [diameter](((64368a97-9392-4dfc-8f6e-fc99ca2c919e)))?
	  \begin{bmatrix}
	  0 & 0 & 1 & 1 & 0 \\
	  0 & 0 & 0 & 1 & 0 \\
	  1 & 0 & 0 & 1 & 1 \\
	  1 & 1 & 1 & 0 & 0 \\
	  0 & 0 & 1 & 0 & 0 \\
	  \end{bmatrix}
	-
	- Provide an example of a graph with a structurally weak tie and motivate your answer.
	-
	- Draw the following graph and compute the clustering coefficient of every node.
	  edge list: $[(a,b), (b,c), (b,d), (c,d), (d,e), (e,f), (f,a)]$
	-
	- Given the bipartite [affiliation graph](((631cc01b-8f07-470d-9924-40500a8a9d40))) in the figure:
	  ((646e354d-0ac1-4806-809d-9d27ca954aa5))
		- Draw the [projected](((64691261-1cc5-4b32-847b-5b8396942cb0))) graph.
		- Give an example of two different affiliation networks - on the same set of people, but with different foci - so that the projected graphs from these two different affiliation networks are the same. This shows how information can be "lost" when moving from the full affiliation network to just the projected graph on the set of people.
	-
	- Suppose you have a valuable piece of information and you want that it spreads quickly on the social network you belong to. Who would you share it with to make the spreading faster and why? (choose between the two for each option)
		- A close friend of yours or an acquaintance?
		- A very sociable or a moderately sociable person?
	-
	- Suppose that some researchers studying educational institutions decide to collect data to address the following two questions:
	  
	  > (a) As a function of $k$, what fraction of Cornell classes have $k$ students enrolled?
	  
	  > (b) As a function of $k$, what fraction of 3rd-grade elementary school classrooms in New York State have $k$ pupils?
	  
	  Which one of these would you expect to more closely follow a power-law distribution as a function of $k$? Give a brief explanation for your
	  answer, using some of the ideas about power-law distributions.
	-
	- Draw a hyper-graph and its corresponding hyper-edge list representation.
	-
	- Consider the social network represented in the figure. Suppose that this social network was obtained by observing a group of people at a particular point in time and recording all their friendship relations. Now suppose that we come back at some point in the future and observe it again. According to the theories based on empirical studies of [triadic closure](((64625526-7abe-416b-8538-8f2d05123946))) in networks, which new edge is most likely present? (I.e. which pair of nodes, that do not currently have an edge connecting them, are most likely to be linked by an edge when we return to take the second observation?) Also, give a brief explanation for your answer.
	-
	- True/False:
		- Any network with N nodes and at least N edges must contain a cycle
		- Any network with N nodes and less than N edges does not contain any cycle
	-
	- If we consider an epidemic spreading on a graph, only the nodes in the connected component of the first infected individuals can be infected. With this in mind, if we consider an epidemic spreading on an Erdos Renyi graph below the percolation threshold, is it possible that a finite fraction of the population will get infected?
	-
	- Consider the degree sequence $k = (1, 3, 5, 3)$:
		- is this a reasonable input to create an unweighted graph without self-loops from the configuration model?
		- What about the sequence $k = (1, 3, 4, 3)$
	-
	- Given the graph in the figure. What is/are the node/s with the highest [betweenness](((631ef02a-be3c-49ea-adc7-d5c938f722f7))) centrality, and which ones have the highest degree centrality?
	  ((646e3a44-2f12-495c-8097-31f72d637c5f))
	-
	- Consider an [ER graph](((646e2aea-4f90-47a5-83c2-0827e9bb2db1))) with $n = 5 \cdot 10^4$ nodes and average degree $k = 100$. How can you approximate its diameter?
	-
	- Explain why the Watts-Strogatz model is able to create networks with high clustering coefficients and small diameter.
	-
	- Show that any partition of a clique has negative [modularity](((6468a11b-78cd-4b64-9e79-96d84f382f47))).
	  id:: 646e3ab0-51ae-4482-9533-074f575b1ff1
	-
	- The older nodes of a Barabasi-Albert network are those with higher degree. (True/False)
	-
	- Does the creation of a new fast road always decrease the total travelling time? If not, provide a counter-example
-
- # Soluzioni
	- ((646e3ab0-51ae-4482-9533-074f575b1ff1))
		- ((646a363f-b4cd-422d-9596-e37857062559))
		- Per una cricca:
			- il grado di ogni nodo è sempre $n - 1$ ($k_i$ e $k_j$).
			- il numero di archi $m$ è $\frac{n(n-1)}2$
		- Sia $Q_C$ la modularità di una cricca.
		- \begin{aligned}
		  Q_C &= \frac{1}{2m} \sum_{ij} \left(a_{ij} - \frac{(n-1)^2}{2m}\right) \delta_{g_i g_j} \\
		  &= \frac{1}{\cancel{2}} \frac{\cancel{2}}{n(n-1)} \sum_{ij} \left(a_{ij} - \frac{(n-1)^{\cancel{2}}}{\cancel{2}} \frac{\cancel{2}}{n\cancel{(n-1)}} \right) \delta_{g_i g_j} \\
		  &= \frac{1}{n(n-1)} \sum_{ij} \left(a_{ij} - \frac{n-1}n\right) \delta_{g_i g_j}
		  \end{aligned}
		- Si prende il caso in cui tutti i nodi appartengono a un solo gruppo
			- $\delta_{g_i g_j} = 1 \;\forall i, j \in N$
			- La modularità per più gruppi sarà sempre minore o uguale al valore di modularità di questo specifico caso.
		- $$Q_C \le \frac{1}{n(n-1)} \sum_{ij} \left(a_{ij} - \frac{n-1}n\right) \cancel{\delta_{g_i g_j}}$$
		- Si distinguono due casi:
			- $i \neq j$ e $a_{ij} = 1$
				- essendo una cricca, c'è sempre un arco tra due nodi diversi
			- $i = j$ e $a_{ij} = 0$
				- non c'è un arco tra un nodo e se stesso
		- \begin{aligned}
		  Q_C &\le \frac{1}{n(n-1)} \left[\sum_{i\neq j} \left(1 - \frac{n-1}n\right) - \sum_i \frac{n - 1}{n} \right] \\
		  \end{aligned}
			- Le sommatorie non hanno più termini indicizzati e possono essere sostituite con prodotti
				- $\sum_{i\neq j} = n(n-1)$
				- $\sum_i = n$
		- \begin{aligned}
		  Q_C &\le \frac{1}{n(n-1)} \left[\cancel{n}(n-1)\cancel{\frac{1}n} - \cancel{n} \frac{n - 1}{\cancel{n}} \right] \\
		  &\le \frac{1}{n(n-1)} \left[(n - 1) - (n - 1)\right] \\
		  &\le 0
		  \end{aligned}