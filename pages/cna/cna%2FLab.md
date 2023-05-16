- # Complex Network Analysis Lab
	- Show your understanding of the basic practical tools needed to analyze a given network, using R or Python (or, alternatively, R/C/Java or any other language you feel comfortable with)
	- You are likely to include/install many libraries (igraph, networkx, ...)
	- gephi is a great tool if you need to analyze/visualize an adequately small network. You can use gephi at this stage to better and quickly visualize the network, but you must focus on other tools to perform the majority of your measures (see next slide)
- ## Objectives
	- You are requested to give a generic description of the network. Calculate the measures and the characteristics below, and plot them whenever it is possible/significant:
		- DONE Distances: average, distribution ((64368a97-14dd-4a64-95fb-cc81a0328d14))
		  :LOGBOOK:
		  CLOCK: [2022-09-13 Tue 18:37:34]--[2022-09-13 Tue 18:37:35] =>  00:00:01
		  :END:
		- TODO Degree  ((6462989a-ec74-4814-ba4f-745fd640511c))
			- DONE average
			- DONE variance/standard deviation
			- TODO degree distribution
				- some fit? Does it follow a power law? If yes, is it in the scale-free regime?
		- DONE Clustering coefficient ((64625143-588e-4dc1-a991-4b27deea3a85))
		  :LOGBOOK:
		  CLOCK: [2022-09-13 Tue 19:19:21]--[2022-09-13 Tue 19:19:22] =>  00:00:01
		  :END:
		- DONE Largest connected component size ((64368a97-8099-48bf-b424-298fc228d1bb))
		- ((64368a97-8099-48bf-b424-298fc228d1bb))
		- DONE [[Degree correlation]]: neutral, assortative, disassortative?
		  :LOGBOOK:
		  CLOCK: [2022-09-13 Tue 19:16:02]--[2022-09-13 Tue 19:16:02] =>  00:00:00
		  :END:
		- Communities
			- Can you properly show them with an appropriate layout?
			- Can you discuss them?
		- DONE [[Centralità]]
		  :LOGBOOK:
		  CLOCK: [2022-09-13 Tue 21:19:27]--[2022-09-13 Tue 21:19:27] =>  00:00:00
		  :END:
		- DONE [[Homophily]]
		- Try to interpret the results of these measures, and comment/discuss results.
- ## TODO Dynamics (optional)
	- Once you have studied your network, and you have a general understanding of its structure, you can use it to simulate some processes
	- We have seen a few:
		- Behavioral cascades
		- Diffusion of innovations
		- Epidemics
		- ...
		- What could you expect to happen over that network when some of these models is simulated?
- ## TODO Random models (optional)
  :LOGBOOK:
  CLOCK: [2022-10-21 Fri 11:51:48]--[2022-10-21 Fri 11:51:49] =>  00:00:01
  :END:
	- You probably need to create your own artificial random networks for comparison purposes:
		- Erdos-Renyi
		- Watts-Strogatz (small-world)
		- Configuration model (degree preserving)
		- Barabasi-Albert (preferential attachment)
		- Stochastic bloc model
	- You can use different generative models, to produce comparisons, varying some parameters (e.g., linking probability, number of edges added at each step, degree distributions, and so on)
	- For some comparisons, you may need to preserve some characteristics (e.g., degree distribution). Try to rewire properly your network in order to shuffle your data.
	- You can perform on such synthetic networks the analysis that has been proposed in the previous slides, to detect differences
	- Try to explain different behaviors
	- You can get inspiration from some of the exercises you solved in the theoretical part of the previous assignment
- ## Datasets
- Hint: before challenging yourself with a “serious” dataset, try to execute your assignment with a smaller one. You can find many of them around
- Once you have developed your code and trained your skills, attack one of the datasets you can find in one of these sources:
	- datasets attached to notebooks we studied during our course (you can expand the analysis we have already studied together)
	- [SNAP](https://snap.stanford.edu/data/index.html)
	- [KONECT](http://konect.cc/)
	- Some networks can also be found on [Kaggle](https://www.kaggle.com/)!
- Make your own selection!
- If previous studies on the dataset you selected are available, use them as a reference or for comparison
- Warning: avoid large datasets (you may suffer of a lack of computational power...)
- Deadline
	- Just remember to submit on moodle your technical report at least three days before the final exam. Use the same folder on moodle to submit your reports (zip them to upload only one file)
	  • Recommendation: use Latex, adopting an article template, and listing the names of the authors