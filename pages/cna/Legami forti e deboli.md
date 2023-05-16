tags:: cna

- # Connessione tra locale e globale
	- Le reti giocano un ruolo importante nel **connettere il locale con il globale** per offrire spiegazioni su come processi semplici al livello di nodi e archi individuali possano avere **effetti a cascata su intere popolazioni.**
		- Come fluisce l'informazione in un social network?
		- Quanto nodi diversi possono giocare ruoli strutturalmente distinti in questo processo?
		- Come queste considerazioni strutturali danno forma all'evoluzione della rete stessa nel tempo?
- # Ipotesi di Granovetter
  id:: 646275b2-6714-42a4-ad0e-ef408992f8ec
	- ## Domanda motivante
		- Come parte della sua tesi di Ph.D nei tardi anni 60, Mark Granovetter intervistò persone che avevano recentemente cambiato dato di lavoro per capire come avessero trovato i loro nuovi lavori.
		- Ha scoperto che:
			- Molte persone apprendevano informazioni che li portavano ai loro attuali lavori tramite **contatti personali**.
			- Questi contatti personali venivano spesso descritti nelle interviste come **conoscenti** invece che amici stretti.
	- La risposta proposta da Granovetter lega due diverse prospettive sulle amicizie lontane:
		- una **strutturale**, che si concentra sul modo in cui queste amicizie si estendano su diverse porzioni dell'intera rete.
		- una **interpersonale**, considerando le conseguenze puramente locali che derivano dal fatto che un'amicizia tra due persone sia forte o debole.
			- Si possono quindi fare delle distinzioni tra i tipi di collegamento:
			  id:: 6382460e-fb94-4ee5-aaaf-f7ed5a836c6d
				- di tipo **locale e interpersonale**, in base a se siano [deboli o forti](((646328e9-442d-4f04-ac0c-fe6650ac3e66)))
				- di tipo **strutturale**, in base a se sia un ((631aefdf-9178-4e44-91a5-69200e94239c)) o no.
	- La risposta trascende il contesto specifico della ricerca del lavoro, e offre un modo di pensare riguardo l'architettura delle reti sociali in modo più generale.
	- > ((631af429-3ced-4079-b376-69bbd3bf171d))
- # Chiusura triadica
  id:: 64625526-7abe-416b-8538-8f2d05123946
	- *Se due persone in una rete sociale hanno un amico in comune, allora c'è una maggiore probabilità che diventino amici tra di loro in futuro.*
	- Il ruolo base della chiusura triadica nelle reti sociali ha motivato la formulazione di misure delle reti sociali per catturarne la prevalenza. Una di queste è il ((64625143-588e-4dc1-a991-4b27deea3a85)).
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
	- ## Chiusura triadica forte
	  id:: 631af503-9746-4c05-aefa-2b1000b877dd
		- Un nodo $A$ viola la **proprietà di chiusura triadica forte** se ha legami forti $A \rightarrow B$ e $A \rightarrow C$, e non c'è nessun arco (che sia forte o debole) $B \rightarrow C$.
		- $A$ soddisfa la proprietà di chiusura triadica forte se non la viola.
		- La proprietà di chiusura triadica forte è troppo estrema perché possiamo aspettarci che tenga attraverso tutti i nodi di una rete sociale grande. Ma può essere utile come astrazione.
- # Ponte
  id:: 646275b2-d730-4377-b20c-44e761e3a1a5
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
	- Opposto concettuale a ((64625526-7abe-416b-8538-8f2d05123946))
		- un arco è un ponte locale precisamente quando **non forma un lato** di un qualunque triangolo nel grafo
	- I ponti locali, specie se grandi, hanno circa lo stesso ruolo dei ponti, anche se in modo meno estremo
		- Forniscono ai loro endpoint accesso a parti della rete, e quindi fonti di informazione da cui sarebbero altrimenti lontani.
		- Ci si può aspettare che se un nodo come $A$ cerchi di trovare informazioni **veramente nuove**, queste potrebbero arrivare inaspettatamente spesso da un amico connesso da un ponte locale.
		  id:: 631af429-3ced-4079-b376-69bbd3bf171d
			- > I gruppi affiatati, anche se pieni di persone pronte ad aiutarsi a vicenda, sono anche quelli che sanno più o meno le stesse cose.
- # Forza dei legami
  id:: 646328e9-442d-4f04-ac0c-fe6650ac3e66
	- Connessioni più forti rappresentano **amicizie più strette e una maggior frequenza di interazione**.
	- Per semplicità concettuale categorizzeremo tutti i collegamenti nella rete sociale come appartenenti a due tipi
		- **legami forti** (corrispondenti ad amicizie)
		- **legami deboli** (corrispondenti ai conoscenti).
	- ![image.png](../assets/image_1662655251394_0.png){:height 354, :width 465}
	- ## ((64625526-7abe-416b-8538-8f2d05123946)) e forza dei legami
		- Se ricordiamo le [argomentazioni a supporto della chiusura triadica](((631a198f-9eb1-4235-9424-01ed661dbc7c))), basate su **opportunità, fiducia e incentivi**, queste agiranno più potentemente quando gli archi coinvolti sono **legami forti** piuttosto che deboli.
		- Assunzione qualitativa:
			- *Se un nodo A ha archi ai nodi B e C e se gli archi sono legami forti, allora è particolarmente probabile che si formi l'arco B-C*.
- # Connessione tra [ponti locali](((631aefdf-9178-4e44-91a5-69200e94239c))) e [legami deboli](((646328e9-442d-4f04-ac0c-fe6650ac3e66)))
  id:: 646357c4-b064-4a5e-92aa-22bbec17f577
	- Se un nodo $A$ in una rete soddisfa la proprietà di ((631af503-9746-4c05-aefa-2b1000b877dd)) ed è coinvolto in almeno due [legami forti](((646328e9-442d-4f04-ac0c-fe6650ac3e66))), allora ogni ((631aefdf-9178-4e44-91a5-69200e94239c)) che vi è coinvolto **deve essere un legame debole.**
	- ## Dimostrazione
		- ![image.png](../assets/image_1662744637303_0.png){:height 339, :width 424}
		- La dimostrazione procede per contraddizione.
		- Si consideri una rete e un nodo $A$ che soddisfa la proprietà di ((631af503-9746-4c05-aefa-2b1000b877dd)) e che è coinvolto in almeno due legami forti.
		- Ora si supponga che esista un ((631aefdf-9178-4e44-91a5-69200e94239c)) $A \rightarrow B$, e che sia un legame forte.
		- Dato che $A$ è coinvolto in almeno due legami forti, e che l'arco $B$ è soltanto uno di questi, **esso deve avere un legame forte a un qualche altro nodo** $C$ .
		- Per cui, c'è un arco $B \rightarrow C$?
		- Dato che l'arco $A \rightarrow B$ è un ponte locale, $A$ e $B$ **non dovrebbero avere amici in comune**, per cui il ponte $B \rightarrow C$ **non dovrebbe esistere.**
		- Questo contraddice la proprietà di chiusura triadica forte: dato che gli archi $A \rightarrow B$ e $A \rightarrow C$ sono entrambi legami forti, il legame $B \rightarrow C$ dovrebbe esistere.
		- Questa contraddizione mostra che **non può esistere un legame forte che sia un ponte locale.**
	- ## Considerazioni
		- Questa argomentazione completa la connessione tra la proprietà locale della forza di legame e la proprietà globale di servire da ponte locale.
		- In quanto tale, ci dà modo di pensare al modo in cui proprietà interpersonali di reti sociali sono collegate a considerazioni più ampie riguardanti la struttura della rete.
		- La chiusura triadica forte è molto forte come assunzione.
			- **Semplificare** è utile quando porta ad affermazioni che sono robuste nella pratica, che abbiano senso come **conclusioni qualitative che reggono in forme approssimative** anche quando le assunzioni vengono rilassate.
			- Di fatto, l'argomentazione matematica può essere riassunta più informalmente e approssimativamente dicendo che nella vita reale **un ponte locale tra nodi A e B tende a essere un legame debole**, perché se non lo fosse, l**a chiusura triadica tenderebbe a produrre scorciatoie** da $A$ a $B$ che **eliminerebbero il suo ruolo come ponte locale.**