slide:: ![ns07](../assets/ns07.pdf)

- Recap:
	- reti reali sono [eterogenee](((64691261-099a-48a0-8e18-6c69cbbc6205)))
	- in-link misura di popolarità
- Caratterizzare la popolarità mostra degli squilibri
	- quasi tutti sono popolari per molti pochi individui
	- poche persone raggiungono un'alta popolarità
	- molte poche persone raggiungono popolarità globale
- Questo fenomeno è intrinseco alla popolarità in sé?
-
- # Power laws #card
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-06-11T22:00:00.000Z
  card-last-reviewed:: 2023-06-11T10:12:13.847Z
  card-last-score:: 1
	- La frazione di pagine web che hanno $k$ in-link è:
		- id:: 647cf8b4-16b7-45f0-9ec8-f0a8166ba847
		  $$f(k) \approx \frac1{k^c} = k^{-c}$$
		-
- ## Preferential attachment #card
  id:: 647cfa91-3c31-4b4b-ba93-3c9ebf8b81b4
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-06-11T22:00:00.000Z
  card-last-reviewed:: 2023-06-11T18:34:06.296Z
  card-last-score:: 1
	- I nodi preferiscono collegamenti a nodi più connessi
	- Esempio:
		- La nostra conoscenza di internet ha un bias verso le pagine popolari, che sono altamente connesse,  per cui è più probabile che il nostro sito punti a pagine che sono state molto linkate.
		- Gli scienziati sono più familiari con paper molto citati (che sono spesso i più importanti), per cui tendono a citare più questi di altri
- # Modello di Barabasi-Albert #card
  id:: 647cd5f7-a502-4356-b841-b2ddd48fbf93
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-06-11T22:00:00.000Z
  card-last-reviewed:: 2023-06-11T10:34:58.974Z
  card-last-score:: 1
	- Le reti reali sono dinamiche e si evolvono nel tempo, in base alle circostanze.
	- Procedura generale:
		- Arriva un nuovo nodo con un certo numero di ceppi di arco, che indicano il numero di futuri vicini del nodo (grado)
		- Gli archi vengono connessi ad alcuni dei vecchi nodi, secondo qualche regola.
	- ## Procedura
	  id:: 647cfb3a-fa0e-4240-b2c9-607bd7b9a41d
		- ### Fase iniziale
		  id:: 647d06a9-e3e7-4e47-be61-32bcbfb3211c
			- Si inizia con un gruppo $m_0$ di nodi, solitamente completamente connessi (cricca)
			  id:: 647cfbd6-8906-46b7-9986-891e3e7368dd
			- A ogni passo si aggiunge un nodo $i$ al sistema, e vengono impostati $m$ link ad alcuni dei nodi più vecchi ($m \le m_0$)
			  id:: 647cfbef-c315-437b-acbc-94a766e7ae70
		- Probabilità che il nuovo nodo $i$ scelga un nodo più vecchio $j$ come vicino:
			- proporzionale al grado $k_j$ di $j$:
				- $$P(i \leftrightarrow j) = \frac{k_j}{\sum_l k_l}$$
		- La procedura termina quando si raggiungono $N$ nodi
	- ## Rich-gets-richer
		- Dato il preferential attachment, i nodi più connessi hanno possibilità più alte di acquisire nuovi link, il che dà loro un vantaggio sempre più grande sugli altri nodi in futuro.
		- È così che si vengono a formare gli hub.
		- Questo fenomeno **dipende strattamente dal preferential attachment**: la sola crescita dei nodi iniziali più connessi non porta da sola alla formazione di hub.
	- ## Non-linear preferential attachment #card
	  card-last-interval:: -1
	  card-repeats:: 1
	  card-ease-factor:: 2.5
	  card-next-schedule:: 2023-06-11T22:00:00.000Z
	  card-last-reviewed:: 2023-06-11T09:49:32.656Z
	  card-last-score:: 1
		- Il modello di Barabasi-Albert usa un preferential attachment lineare: la probabilità di connessione è proporzionale al grado
		- È possibile creare modelli con preferential attachment non lineare.
		- ### Procedura
			- {{embed ((647d06a9-e3e7-4e47-be61-32bcbfb3211c))}}
			- Probabilità che il nuovo nodo $i$ scelga un nodo più vecchio $j$ come vicino:
				- Proporzionale **a una potenza** $\alpha$ del grado $k_j$ di $j$:
					- $$P(i \leftrightarrow j) = \frac{k_j^\alpha}{\sum_l k_l^\alpha}$$
		- Al variare di $\alpha$:
			- Se $\alpha = 1$ si ottiene il linear preferential attachment
			- Se $\alpha < 1$, la probabilità dei link non cresce sufficientemente con il grado, per cui il vantaggio dei nodi con grado alto è minore. Per cui, **la distribuzione dei gradi non è heavy-tail e gli hub spariscono**
			- Se $\alpha > 1$, i nodi di grado elevato accumulano link molto più velocemente rispetto ai nodi di grado inferiore.
				- Uno dei nodi sarà connesso a una frazione di tutti gli altri nodi
			- Per $\alpha > 2$ un singolo nodo potrebbe essere connesso a tutti gli altri nodi (**winner-takes-all effect**), con tutti gli altri nodi che restano di grado basso.
			- #### Conclusione
				- Il preferential attachment non lineare fallisce nel generare hub. Il preferential attachment lineare è il migliore.
				- Il problema è che un attachment strettamente proporzionale sembra poco realistico
	- ## Limiti del preferential attachment
		- Dà un pattern fisso per le distribuzioni di grado: la curva è la stessa per qualunque scelta di parametri del modello. Le distribuzioni di grado nel mondo reale posso decadere più velocemente o lentamente.
		- **Gli hub sono i nodi più vecchi**
			- i nuovi nodi non possono oltrepassare il proprio grado.
		- **Non crea molti triangoli**
			- Il coefficiente di clustering medio è molto più basso rispetto a quello di molte reti reali.
		- **I nodi e i link sono solo aggiunti**
			- Nelle reti reali questi possono anche essere eliminati
		- Dato che ogni nodo è collegato a nodi più vecchi, **la rete consiste di una singola componente connessa.** Molte reti reali hanno componenti multiple.
	- ## Difetto del preferential attachment
		- che succede se il nodo non ha vicini (grado zero)?
		- non arriverà mai ad avere connessioni con altri nodi
		- non è un problema per la condizione iniziale standard: il sottografo iniziale è completo, per cui ogni nodo ha grado non-zero
		- Se la rete fosse diretta e la probabilità di link fosse proporzionale all'in-degree?
			- male, dato che ogni nuovo nodo ha in-degree zero, per cui non verrebbe mai connesso ad altri nodi
- # Attractiveness model #card
  id:: 647d0650-7584-48e2-aa73-2d718f44621e
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-06-11T22:00:00.000Z
  card-last-reviewed:: 2023-06-11T10:36:14.567Z
  card-last-score:: 1
	- ### Procedura
		- {{embed ((647d06a9-e3e7-4e47-be61-32bcbfb3211c))}}
		- Probabilità che il nuovo nodo $i$ scelga un nodo più vecchio $j$ come vicino:
			- Proporzionale alla somma del grado $k_j$ di $j$ e di una attrattività $A$, che indica un appeal intrinseco:
				- $$P(i \leftrightarrow j) = \frac{A + k_j}{\sum_l (A + k_l)}$$
	- Per $A = 0$ si torna al Barabasi-Albert
	- Per ogni valore di $A$ si ottengono reti con distribuzione di grado heavy-tail
	- Il pattern della distribuzione **cambia con** $A$, per cui è possibile fare match con distribuzioni di reti reali, a differenza del modello BA
	- ### Difetto dell'Attractiveness Model
		- Gli hub sono i nodi più vecchi, il che è irrealistico.
			- Nella rete, nuove pagine possono superare le vecchie (es. Google)
			- Nella scienza, nuovi paper possono avere più successo di (molti) vecchi paper
		- **Ragione**: ogni nodo ha il suo appeal individuale
- # Fitness Model
  id:: 647d0895-5ac7-4b3a-91a6-77245a1205c8
	- ### Procedura
		- {{embed ((647d06a9-e3e7-4e47-be61-32bcbfb3211c))}}
		- Probabilità che il nuovo nodo $i$ scelga un nodo più vecchio $j$ come vicino:
			- Proporzionale al prodotto del grado $k_j$ con una fitness $\eta_j$, che indica l'appeal intrinseco di $j$:
				- $$P(i \leftrightarrow j) = \frac{\eta_j k_j}{\sum_l \eta_l  k_l}$$
	- I valori di fitness sono estratti da una distribuzione $\rho(\eta)$ e assegnati a ogni nuovo nodo
		- Il fitness è un **fattore** nella probabilità di link, non un addendo
		- Il fitness è caratteristico di ogni nodo e non è costante
	- ### Risultati
		- Se la distribuzione $\rho(\eta)$ ha supporto **finito**, ovvero il fitness è distribuito su un range finito di valori, la distribuzione dei gradi della rete è heavy-tailed
		- Se la distribuzione $\rho(\eta))$ ha supporto **infinito**, ovvero il fitness è distribuito su un range infinito di valori, il nodo con il fitness più grande attrae tutti i link (**monopolio**)
		- I nodi con fitness grande possono acquisire un grado alto anche se introdotti tardi nel sistema.
	- ### Difetto
		- Il modello BA non genera molti triangoli
		- Per chiudere triangoli è necessario impostare un link tra due vicini di un nodo, mentre nel modello BA i link sono piazzati in base al grado, a prescindere di se i futuri vicini avranno vicini in comune
		- Soluzione: introdurre un meccanismo per la chiusura triadica nel modello
- # Random walk model
  id:: 647d0cef-047f-48db-b506-eab886c638fa
	- ### Procedura
		- {{embed ((647d06a9-e3e7-4e47-be61-32bcbfb3211c))}}
		- Il primo link usa come target un nodo $j$ scelto casualmente
		- Dal secondo link in poi:
			- Con probabilità $p$ il link viene impostato a un vicino di $j$, scelto casualmente
			- Con probabilità $1 - p$ il link viene impostato a un nodo scelto casualmente
	- ### Risultati
		- La distribuzione dei gradi è heavy-tailed
		- Il coefficiente di clustering medio è molto più alto in reti BA (più sono grandi, maggiore la probabilità $p$ di chiusura triadica)
		- Quando la probabilità di chiusura triadica $p$ è abbastanza grande da formare molti triangoli $(p - 1)$ la rete ha **struttura di comunità**
			- composta da gruppi coesi di nodi, vagamenti connessi tra di loro
	- ### Conclusioni
		- Se i link sono messi casualmente come sembra, come fa il modello a generare hub?
			- Scegliere un nodo casuale e un vicino casuale equivale a scegliere un link casuale
			- La probabilità che gli estremi di un link scelto a caso abbiano un certo grado è **proporzionale al grado**.
		- Il meccanismo di chiusura triadica del modello random walk induce effettivamente il preferential attchment.
		- Il preferential attachment può essere indotto da semplici meccanismi basati su scelte casuali. Non è necessario richiedere il grado del nodo, né una stretta espressione della probabilità del link
- # Rank model
  id:: 647d8d62-cac1-4382-a7d0-49d31be1ce24
	- ## Difetto del preferential attachment
		- Il modello BA implica che i nodi abbiano una percezione di quanto siano importanti gli altri nodi, ovvero di quanto sia grande il loro grado
		- **Obiezione**: nel mondo reale non c'è una percezione simile del valore assoluto delle cose: è molto più semplice percepire un valore relativo
		- Soluzione: Rankning
	- ## Procedura
		- I nodi ricevono un rank in base a una proprietà di interesse (es. età, grado). Il rango del nodo $i$ è $R_i$
		- {{embed ((647d06a9-e3e7-4e47-be61-32bcbfb3211c))}}
		- Probabilità che il nuovo nodo $i$ scelga un nodo più vecchio $j$ come vicino:
			- Proporzionale a una potenza del rango di $j$:
				- $$P(i \leftrightarrow j) = \frac{R_j^{-\alpha}}{\sum_l R_l^{-\alpha}}$$
	- ## Risultato
		- I nodi di rango elevato (con valori **bassi** di $R$) hanno probabilità alta di essere connessi, molto più alta rispetto a nodi di rango basso.
		- Il modello genera reti con hub, per **qualunque valore** dell'esponente $\alpha$ e **qualunque proprietà** usata per il rango dei nodi.
- # Imprevidibilità dell'effetto Rich-Get-Richer
	- Le leggi di potenza sono prodotte da effetti di feedback
	- Le fasi iniziali del processo che danno vita alla popolarità di un nodo sono relativamente fragili
	- Concentrandosi sul mercato culturale, si può predire la popolarità di una canzone, film, ecc. ?
	- Ci si possono aspettare fluttuazioni iniziali: questo porta a imprevedibilità
	- ## Predire l'emergenza di hub
		- Si può predire che una legge di potenza emerga dopo un po', e si può quindi predire che ci saranno hub
		- Ma quali hub?
		- Predire il successo di un individuo non è come predire che qualche individuo avrà successo globale
- # Long tail
	- La popolarità può essere caratterizzata da leggi di potenza
	- Questo significa che un piccolo insieme di elementi è enormemente popolare
	- Se si possono scommettere soldi su nicchie o hit, che cosa faresti?
	- Idea di Chris Anderson:
		- non concentrarsi su hit, ma provare a stimare le vendite di tutte le nicchie
	- ## Legge di Zipf
		- ((647d964d-7565-409c-ab57-9c9331663e72))
			- Come funzione di $k$, quale frazione di elementi hanno popolarità esattamente $k$?
		- ((647d969a-d3ad-4ea5-b911-f086b67eabd0))
			- **Grafico di Zipf**
			- Invertendo gli assi:
				- Come funzione $j$ quanti elementi hanno popolarità almeno $k$?
			- Concentrarsi sulla "coda lunga"
				- Quando si muovono volumi di vendite di molti prodotti di nicchia, è necessario comparare se ci sia significativamente più area sotto la parte sinistra della curva (hits) o la destra (prodotti di nicchia)
		- La legge di Zipf si riferisce alla dimensione $k$ come all'occorrenza di un evento relativamente al suo rango $j$
			- Dice che la dimensione della $j$-esima occorrenza più grande dell'evento è inversamente proporzionale al suo rango
			- id:: 647d97c0-5489-42b6-be0c-93279c34b5e2
			  $$k \approx j^{-b}$$
				- con $b$ solitamente vicino a 1
	- ## Legge di Pareto
		- Pareto era interessato alla distribuzione di redditi
		- Invece di chiedersi quale fosse il $j$-esimo reddito più grande, si è focalizzato su quante persone avessero un reddito più grande di $j$
		- La legge di Pareto è una distribuzione di probabilità cumulativa:
			- id:: 647d9871-14e3-40da-a0b1-250c71ca719f
			  $$P(K > k) \approx k^{-\gamma}$$
	- ## Tre leggi simili
		- Zipf
			- ((647d97c0-5489-42b6-be0c-93279c34b5e2))
		- Pareto
			- ((647d9871-14e3-40da-a0b1-250c71ca719f))
		- Power law
			- ((647cf8b4-16b7-45f0-9ec8-f0a8166ba847))
		- È possibile dimostrare che $c = 1 + \gamma$ e che $\gamma = \frac1b$