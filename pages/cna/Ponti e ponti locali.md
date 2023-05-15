tags:: cna

- # Ponte
	- Un arco $A \rightarrow B$ è un **ponte** se cancellandolo $A$ e $B$ verrebbero a trovarsi in due [componenti]([[Connettività e componenti]]) distinte.
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