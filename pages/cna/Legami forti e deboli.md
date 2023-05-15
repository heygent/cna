tags:: cna

- # Connessione tra locale e globale
	- Le reti giocano un ruolo importante nel **connettere il locale con il globale** per offrire spiegazioni su come processi semplici al livello di nodi e archi individuali possano avere **effetti a cascata su intere popolazioni.**
		- Come fluisce l'informazione in un social network?
		- Quanto nodi diversi possono giocare ruoli strutturalmente distinti in questo processo?
		- Come queste considerazioni strutturali danno forma all'evoluzione della rete stessa nel tempo?
- # Ipotesi di Granovetter
	- ## Domanda motivante
		- Come parte della sua tesi di Ph.D nei tardi anni 60, Mark Granovetter intervistò persone che avevano recentemente cambiato dato di lavoro per capire come avessero trovato i loro nuovi lavori.
		- Ha scoperto che:
			- Molte persone apprendevano informazioni che li portavano ai loro attuali lavori tramite **contatti personali**.
			- Questi contatti personali venivano spesso descritti nelle interviste come **conoscenti** invece che amici stretti.
	- La risposta proposta da Granovetter lega due diverse prospettive sulle amicizie lontane:
		- una **strutturale**, che si concentra sul modo in cui queste amicizie si estendano su diverse porzioni dell'intera rete.
		- una **interpersonale**, considerando le conseguenze puramente locali che derivano dal fatto che un'amicizia tra due persone sia forte o debole.
			- Si possono quindi fare delle distinzioni tra i tipi di collegamenti:
			  id:: 6382460e-fb94-4ee5-aaaf-f7ed5a836c6d
				- di tipo **locale e interpersonale**, in base a se siano [deboli o forti]([[Forza dei legami]])
				- di tipo **strutturale**, in base a se siano [ponti locali]([[Ponti e ponti locali]]) o no.
	- La risposta trascende il contesto specifico della ricerca del lavoro, e offre un modo di pensare riguardo l'architettura delle reti sociali in modo più generale.
	- > ((631af429-3ced-4079-b376-69bbd3bf171d))
- # Ponte
	- Un arco $A \rightarrow B$ è un **ponte** se cancellandolo $A$ e $B$ verrebbero a trovarsi in due [componenti](((64368a97-8099-48bf-b424-298fc228d1bb))) distinte.
	- Quest'arco è **l'unico percorso** tra i suoi endpoint, i nodi $A$ e $B$.
	- ![image.png](../assets/image_1662709688813_0.png)
	- I ponti sono presumibilmente **estremamente rari** in reti sociali vere.
		- > Potresti avere un amico da un background molto diverso, e può sembrarti che la vostra amicizia sua l'unica cosa che collega il tuo mondo al suo, ma ci si aspetta in realtà che ci siano **altri cammini con più passi difficili da scoprire che si estendono per quei mondi**.
- # Ponte locale
  id:: 631aefdf-9178-4e44-91a5-69200e94239c
	- ![image.png](../assets/image_1662710320029_0.png){:height 164, :width 209}
	- Un arco $A \rightarrow B$ è un **ponte locale** se i suoi endpoint $A$ e $B$ non hanno amici in comune.
	- In altre parole, cancellare l'arco aumenterebbe la ((6319be1d-d038-4df4-ae99-dc9ec8844242)) tra A e B di un valore $> 2$.
	- **estensione (span)** di un ponte locale
		- distanza a cui gli endpoint si troverebbero l'uno dall'altro se il ponte fosse cancellato.
	- Opposto concettuale a [[Chiusura triadica]]
		- un arco è un ponte locale precisamente quando **non forma un lato** di un qualunque triangolo nel grafo
	- I ponti locali, specie se grandi, hanno circa lo stesso ruolo dei ponti, anche se in modo meno estremo
		- Forniscono ai loro endpoint accesso a parti della rete, e quindi fonti di informazione da cui sarebbero altrimenti lontani.
		- Ci si può aspettare che se un nodo come $A$ cerchi di trovare informazioni **veramente nuove**, queste potrebbero arrivare inaspettatamente spesso da un amico connesso da un ponte locale.
		  id:: 631af429-3ced-4079-b376-69bbd3bf171d
			- > I gruppi affiatati, anche se pieni di persone pronte ad aiutarsi a vicenda, sono anche quelli che sanno più o meno le stesse cose.