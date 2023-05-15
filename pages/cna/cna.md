icon:: 🌐
banner:: https://images.unsplash.com/photo-1545987796-200677ee1011?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80
color:: "#7cdeff"
public:: true

- # Flashcard
  collapsed:: true
	- {{cards (and (page-tags cna) [[card]])}}
- # Syllabus
	- # Introduction
	  date:: [[2023-02-07]]
	  slide:: ![ns01.pdf](../assets/Lecture01ns01_1679220302961_0.pdf)
	  refs:: [ns1 Chapter 1](((6422e720-946a-4c05-a38c-97f2f7b238a6)))
		- Meaning and examples of complexity
		- networks and complexity
		- examples of applications of network theory
	- # [[Grafo]]
	  date:: [[2023-03-03]]
	  slide:: ![ns02.pdf](../assets/Lecture03ns02_1679220312387_0.pdf)
		- ((6416dcb6-cf08-4329-8e18-c6e6ee5a5b17))
			- node
			- edges
			- cliques
			- subgraphs
			- ((6422f672-3d23-4979-9b1e-299afce67298))
				- ((64368a97-1853-46f2-946d-aba0b766a52e))
				- ((64368a97-78f5-40da-9106-66f02375b7b1))
				- ((64368a97-5d3e-4c20-8c62-6c42ceac80f6))
				- ((64368a97-f886-49ab-ac70-c7ee24f76e37))
			- ((6422f914-29f3-46f4-916c-35a9f825fdb7))
				- ((64368a97-1f6c-45e5-9071-f0d6ff26a06d))
				- ((6422fb58-b14c-4f73-a8ce-c547d160c906))
				- ((64368a97-7c8d-411c-a1ab-d08880fe1e29))
				- ((64368a97-a071-42ad-9844-7d0ec1cf7814))
			- ((64230819-c4a5-41cb-8c3c-1f5aa77033be))
				- ((64368a97-8099-48bf-b424-298fc228d1bb))
				- ((64368a97-14dd-4a64-95fb-cc81a0328d14)) and [[BFS]]
				- ((64368a97-9392-4dfc-8f6e-fc99ca2c919e))
				- small world effect
				- ((64625143-588e-4dc1-a991-4b27deea3a85))
		- Rappresentazioni di reti
			- adjacency matrix
			- adjacency list
			- edge list
	- # [[Legami forti e deboli]]
		- date:: [[2023-03-06]]
		  slide:: ![ns03.pdf](../assets/Lecture04ns03_1679220321358_0.pdf)
		- [[Ipotesi di Granovetter]]
		- [[Chiusura triadica]]
		- ((64625143-588e-4dc1-a991-4b27deea3a85))
		- [[Ponti e ponti locali]]
		- [[Ponti locali e legami deboli]]
		- [[Validazione empirica dell'ipotesi di Granovetter]]
	- # [[Homophily]]
	  date:: [[2023-03-08]]
	  slide:: ![ns04.pdf](../assets/Lecture06ns04_1679220329786_0.pdf)
		- [[Homophily]]
		- Modularity
		- Assortativity
		- Degree assortativity
		- Affililation networks
	- # [[Centralità]]
	  slide:: ![ns05.pdf](../../assets/ns05_1684057975234_0.pdf)
		- Centralità
		- ((64615afb-c2a1-4b0b-866d-ffb62d751cb7))
		- ((64615285-85e9-4b2b-ad5c-7236514d5142))
		- ((64616108-44d8-4246-99b7-7018f4cf99de))
		- ((646165e2-153c-4b4a-a1f8-eddf930fdb9e))
		- ((646166f8-7fe7-4cbc-a061-f5311a8fd698))
		- [Calculating betweenness values](((6461685e-61a0-4ca8-8e40-60cdefd48def)))
	- # [[Modelli generativi]]
	  date:: [[2023-03-15]]
	  slide:: ![ns06.pdf](../../assets/ns06_1684096378817_0.pdf)
		- Recap of real-world network properties
		- Erdos-Renyi and Gilbert random graphs
			- definition
			- percolation threshold with proof
			- degree distribution
			- connectedness transition
			- diameter
			- clustering coefficient)
		- Configuration model
			- definition
			- clustering coefficient
			- relation to the Erdos-Renyi model
		- Watts-Strogatz model
			- definition
			- clustering coefficient and diameter
			- degree distribution
		- stochastic block model
			- definition
			- relation to the Erdos-Renyi model
	- # Rich get richer
	  date:: [[2023-03-20]]
	  slide:: ![ns07.pdf](../assets/Lecture10ns07_1679220312388_4.pdf)
		- the emergence of power law in real-world networks
		- preferential attachment
		- Barabasi-Albert model
			- definition
			- degree distribution with proof
			- clustering coefficient and diameter
		- notions of the generalizations of the preferential attachment
			- non-linear PA
			- attractivness model
			- fitness model
			- random walk model
			- rank model
		- rich get richer paradigm in real-world settings.
	- # Epidemics
		- ## Part 1
		  date:: [[2023-03-27]]
		  slide:: ![ns09.pdf](../../assets/ns09_1684096479483_0.pdf)
			- Reproductive number R0
			- compartimental models (SI, SIS, SIR)
			- SIR epidemic percolation
		- ## Part 2
		  date:: [[2023-03-29]]
		  slide:: ![ns10.pdf](../../assets/ns10_1684096534361_0.pdf)
			- Epidemics in heterogeneous networks
			- The role of hubs
			- Compartimental models on networks
			- Degree compartimental model
			- Epidemic threshold
			- Introduction to contact networks
			- Immunization strategies
	- # Community detection
		- ## Part 1
		  date:: [[2023-04-05]]
		  slide:: ![ns12.pdf](../../assets/ns12_1684096551537_0.pdf)
			- Definition of communities
			- Optimization approach (Cut, RatioCut, Modularity)
			- Bayesian approach to community detection and stochastic block model
		- ## Part 2
		  date:: [[2023-04-12]]
		  slide:: ![ns13.pdf](../../assets/ns13_1684096558663_0.pdf)
			- Hierarchical clustering
			- Node embeddings
			- Spectral clustering;
		- ## Part 3
		  date:: [[2023-04-17]]
		  slide:: ![ns14.pdf](../../assets/ns14_1684096576446_0.pdf)
			- Spectral clustering and the number of communities
			- DeepWalk algorithm
	- # Cascading behaviors
	  date:: [[2023-04-19]]
	  slide:: ![ns15.pdf](../../assets/ns15_1684096590461_0.pdf)
		- Diffusion in networks
		- Cascades and clusters
		- The role of weak ties
		- Heterogeneous cascades
	- # Link analysis and web search
	  date:: [[2023-04-24]]
	  slide:: ![ns16.pdf](../../assets/ns16_1684096604012_0.pdf)
		- Page Rank algorithm
		- Hits algorithm
		- Spectral analysis of the two algorithms
		- Random walks and page rank
		-
	- # Game theory and traffic networks
	  date:: [[2023-05-03]]
	  slide:: ![ns18.pdf](../../assets/ns18_1684096615827_0.pdf)
		- Games and payoff matrix
		- Best response strategy
		- Nash equilibrium
		- Pareto optimum
		- Traffic at equilibrium
		- Difference between Nash equilibrium and social optimum on a traffic network
		-
- # Libri
	- ![ns1](../../assets/ns1_1679941479833_0.pdf): Menczer, Fortunato, Davis, A First Course in Network Science, Cambridge University Press, 2020
	- ![ns2](../../assets/ns2_1679941488766_0.pdf): Easley and Kleinberg, Networks, Crowds, and Markets: Reasoning About a
	   Highly Connected World, Cambridge University Press, 2010