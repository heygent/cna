tags:: cna

- Nelle reti sociali è comune che una conoscenza in comune tra due persone porti i suoi due conoscenti a conoscersi.
- **Coefficiente di clustering di un nodo**
	- La frazione di coppie dei vicini del nodo che sono connesse l'una all'altra.
	- Se $N_i$ è l'insieme dei vicini di $i$, e $\tau(i)$ è il numero di triangoli che coinvolgono $i$:
- $$C(i) = \frac{\tau(i)}{\tau_{\text{max}}(i)} = \frac{\tau(i)}{\binom{k_i}{2}}
  = \frac{2\tau(i)}{k_i(k_i - 1)} : |N_i| = k_i$$
- **Coefficiente di clustering di una rete**
	- media dei coefficienti di clustering di tutti i nodi.
	- $$C = \frac{\sum_{i:k_i > 1} C(i)}{N_{k > 1}}$$
- Il coefficiente di clustering di un nodo A può anche essere definito come la *probabilità che due amici di A selezionati casualmente siano amici tra loro*.
- Alcune reti, es. social network, tendono ad avere coefficienti di clustering alti per la [[Chiusura triadica]]: ci conosciamo tramite amici in comune.
- Altre reti, es. bipartite e tree-like hanno coefficienti di clustering bassi.
- ## Chiudere triangoli
	- Se guardiamo la rete per un periodo di tempo più lungo, possiamo osservare diversi archi formarsi tramite la chiusura triadica, mentre altri si formano anche se i due endpoint non hanno vicini in comune.
	- CC alto
		- molto frequente in reti sociali ("transitività delle amicizie")
	- CC basso
		- se comparato con il CC in un grafo generato casualmente - un grafo casuale del genere deve avere lo stesso numero di nodi, e un uguale numero di archi rimescolati
	- Dati $G$, $G_R$ randomizzazione di $G$, il coefficiente di clustering è "alto" se:
		- $$CC(G) > > CC(G_R)$$