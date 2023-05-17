tags:: cna

- Un algoritmo di layout di una rete posiziona i nodi su di un piano per visualizzare la struttura della rete.
- Ci sono diversi algoritmi di layout. Quelli più comunemente usati sono gli algoritmi di tipo **force-directed layout** (o spring layout):
	- i nodi connessi sono posizionati vicini
	- gli archi hanno lunghezze simili
	- gli incroci tra archi vengono minimizzati
- Si ottiene questo risultato simulando un sistema fisico dove i nodi adiacenti sono connessi da molle e i non-adiacenti si respingono.
- La struttura comunitaria della rete può essere rivelata in questo modo se la rete non è troppo densa o troppo grande.