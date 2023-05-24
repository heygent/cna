- ![Testo](../assets/cna_exam_simulation_may_2022.pdf)
- #.ol-nested
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
	- Consider an ER random graph with $n$ nodes and connecting probability equal to $p$. What is the expected [clustering coefficient](((64625143-588e-4dc1-a991-4b27deea3a85)))? How does this result relate to the clustering coefficient observed in real-world networks?
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
	- Given the bipartite affiliation graph in the figure:
	  ((646e354d-0ac1-4806-809d-9d27ca954aa5))
		- Draw the [projected](((64691261-1cc5-4b32-847b-5b8396942cb0))) graph.
		- Give an example of two different affiliation networks - on the same set of people, but with different foci - so that the projected graphs from these two different affiliation networks are the same. This shows how information can be "lost" when moving from the full affiliation network to just the projected graph on the set of people.
	-
	- Suppose you have a valuable piece of information and you want that it spreads quickly on the social network you belong to. Who would you share it with to make the spreading faster and why? (choose between the two for each option)
		- A close friend of yours or an acquaintance?
		- A very sociable or a moderately sociable person?
	-
	- Suppose that some researchers studying educational institutions decide to collect data to address the following two questions:
	  
	  > (a) As a function of k, what fraction of Cornell classes have k students enrolled?
	  
	  > (b) As a function of k, what fraction of 3rd-grade elementary school classrooms in New York State have k pupils?
	  
	  Which one of these would you expect to more closely follow a power-law distribution as a function of k? Give a brief explanation for your
	  answer, using some of the ideas about power-law distributions.