tags:: cna

- Quali sono i meccanismi per cui i nodi vanno e vengono, e gli archi si formano e svaniscono?
- Il ruolo base della chiusura triadica nelle reti sociali ha motivato la formulazione di misure semplici delle reti sociali per catturare la loro prevalenza. Una di queste è il [[coefficiente di clustering]].
	- Quanto più fortemente la chiusura triadica opera nel vicinato del nodo, più il coefficiente di clustering tende a essere alto.
- ## Motivazioni
  id:: 631a198f-9eb1-4235-9424-01ed661dbc7c
	- Intuitivamente molto naturale, ma l'esperienza suggerisce alcune ragioni basilari psico-sociali sul perché operi:
		- **Opportunità**
			- se A spende tempo sia con B che con C, c'è una possibilità maggiore che finiscano per conoscersi e per potenzialmente diventare amici.
		- **Fiducia**
			- B e C sono amici con A: hanno le basi per fidarsi l'uno dell'altro che due persone casuali potrebbero invece non avere.
		- **Incentivo**
			- se A è amico con B e C, allora diventa una fonte di stress latente se B e C non sono amici.
	- Ci sono manifestazioni empiriche che si mostrano in modi naturali ma preoccupanti in dati sulla salute pubblica.
	- Ad esempio, è stato rilevato che le ragazze adolescenti con un basso coefficiente di clustering nella loro rete di amici hanno significativamente più probabilità di contemplare il suicidio rispetto a quelle il cui coefficiente di clustering è alto.
	- La struttura delle connessioni sociali è un indicatore di eventi catastrofici.
- # Chiusura triadica forte
  id:: 631af503-9746-4c05-aefa-2b1000b877dd
	- Un nodo $A$ viola la **proprietà di chiusura triadica forte** se ha legami forti $A \rightarrow B$ e $A \rightarrow C$, e non c'è nessun arco (che sia forte o debole) $B \rightarrow C$.
	- A soddisfa la proprietà di chiusura triadica forte se non la viola.
	- La proprietà di chiusura triadica forte è troppo estrema perché possiamo aspettarci che tenga attraverso tutti i nodi di una rete sociale grande. Ma può essere utile come astrazione.