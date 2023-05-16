tags:: cna

- # Misure di centralità
	- Misura di importanza di un nodo
	- {{embed ((6422fb58-b14c-4f73-a8ce-c547d160c906))}}
	- ## Closeness
	  id:: 631eef52-ba3a-4806-beb0-fea4f9f0e90e
		- idea: un nodo è più centrale quanto più **è vicino** a tutti gli altri nodi in media
		- $$g_i = \frac{1}{\sum_{j \neq i} \mathcal{l}_{ij}}$$
			- dove $\mathcal{l}_{ij}$ è la distanza tra i nodi $i$ e $j$
			  id:: 64368a97-1bc1-47cb-a2bf-bf9ed2be5e4e
	- ## Betweenness
	  id:: 631ef02a-be3c-49ea-adc7-d5c938f722f7
		- idea: un nodo è più centrale quanto più **è attraversato da cammini.**
		- $$b_i = \sum_{h \neq j \neq i} \frac{\sigma_{hj}(i)}{\sigma_{hj}}$$
			- $\sigma_{hj}$
				- numero di cammini più brevi tra $h$ e $j$
			- $\sigma_{hj}(i)$
				- numero di cammini più brevi tra $h$ e $j$ che passano per $i$
		- ![image.png](../assets/image_1662972284782_0.png)
			- gli **hub** solitamente hanno betweennes alta
			- ci possono essere nodi con betweennes alta **che non sono hub**
		- **link betweenness**
			- frazione di cammini più brevi tra tutte le possibili coppie di nodi che passano per un determinato arco
- # Distribuzione di centralità
  id:: 64615afb-c2a1-4b0b-866d-ffb62d751cb7
	- in reti piccole ha senso chiedersi quali nodi o archi siano i più importanti
	- in reti grandi non tanto
	- soluzione: **approccio statistico**
	- invece di concentrarsi su nodi e link individuali, si considerano **classi** di nodi e archi con proprietà simili
	- ![image.png](../assets/image_1662974454475_0.png){:height 163, :width 410}
		- $n_k$
			- numero di nodi con grado $k$
		- $f_k = \frac{n_k}{N}$
			- frequenza del grado $k$
		- per $N$ grandi, la frequenza $f_k$ diventa la **probabilità** $p_k$ di avere il grado $k$
		- **distribuzione di probabilità**
			- grafico della probabilità $p_k$ rispetto a $k$
	- ## Distribuzione cumulativa
		- Se la variabile non è intera (es. ((631ef02a-be3c-49ea-adc7-d5c938f722f7))) il range di una variabile può essere diviso in intervalli (bin) per poi contare quanti valori ricadono in ciascun intervallo.
		- **distribuzione cumulativa**
			- la probabilità che la variabile assuma valori *più grandi* di $x$ come funzione di $x$
			- si computa sommando le frequenze della variabile all'interno degli intervalli alla destra di $x$
				- $$P(x) = \sum_{v \geq x} \mathcal{f}_v$$
		- **scala logaritmica**
			- utile a rappresentare range di valori molto ampi
			- si riportano i logaritmi dei valori sulle assi delle $x$ e delle $y$
		- **distribuzione heavy-tail**
			- la variabile va da valori piccoli a grandi
	- ## [Degree](((6422fb58-b14c-4f73-a8ce-c547d160c906))) distribution
		- ![image.png](../assets/image_1662974968197_0.png)
		- **heterogeneity**
			- parametro che indica l'ampiezza della distribuzione
			- $$\mathcal{k} = \frac{\lang k^2 \rang}{\lang k \rang^2}$$
			- {{embed ((631eee28-2fed-4f1c-a38b-9e0156115091))}}
			- $$\lang k^2 \rang = \frac{\sum_i k_i^2}{N}$$
			- se la maggior parte dei gradi hanno lo stesso valore, ad esempio $k_0$:
				- $\lang k \rang \approx k_0, \, \lang k^2 \rang \approx k^2_0$
					- $\Longrightarrow \mathcal{k} \approx 1$
			- se la distribuzione è molto eterogenea
				- $\mathcal{k} >> 1$
- # Paradosso dell'amicizia #card
  id:: 64615285-85e9-4b2b-ad5c-7236514d5142
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-05-15T22:00:00.000Z
  card-last-reviewed:: 2023-05-15T01:42:49.924Z
  card-last-score:: 1
	- ((6461509d-f72e-4f72-a403-19eb82ccf158))
		- Scegliendo nodi casualmente, Tom ha la stessa probabilità di essere pescato di tutti gli altri.
		- Scegliendo collegamenti casualmente, Tom ha una probabilità **più alta** di essere pescato.
		- Seguendo i collegamenti la probabilità di incontrare un hub aumenta.
		- > I nostri amici hanno più amici di noi, in media
- # Ultra-small worlds #card
  id:: 64616108-44d8-4246-99b7-7018f4cf99de
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-05-15T22:00:00.000Z
  card-last-reviewed:: 2023-05-15T01:43:32.762Z
  card-last-score:: 1
	- ((64616502-469d-427b-8963-bf47402024a1))
	- In reti reali, molti dei cammini più brevi passano per hub
	- Esempio: trasporto aereo
		- Potrebbero non esserci rotte dirette tra l'aeroporto A e B (se sono piccoli), ma può essere possibile arrivare da A a B tramite un aeroporto hub C
	- La proprietà di small world è tipica della maggior parte delle reti di interesse
	- **Se la rete ha hub, i camini sono molto brevi.**
- # Robustness #card
  id:: 646165e2-153c-4b4a-a1f8-eddf930fdb9e
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-05-15T22:00:00.000Z
  card-last-reviewed:: 2023-05-15T01:43:21.073Z
  card-last-score:: 1
	- il fallimento di alcuni componenti non influenza il funzionamento del sistema
	- per verificare la robustezza di una rete, rimuoviamo nodi o archi e verifichiamo che cosa succede alla sua struttura.
	- punto chiave: ((64368a97-8099-48bf-b424-298fc228d1bb))
		- se internet non fosse connesso, sarebbe impossibile trasmettere segnali (es. email) tra router in diverse componenti.
	- ## Robustness test
		- verificare come la connettività della rete viene afflitta mano a mano che nodi vengono rimossi
		- si fa il grafico della dimensione relativa $S$ del ((6319c11b-bddf-4fbb-bf24-9689c9e2f021)) come funzione della frazione di nodi rimossi.
		- si suppone che la rete sia inizialmente connessa
			- un solo componente
			- $S = 1$
		- mano a mano che più nodi (e link) vengono rimossi, la rete si spezza in componenti e $S$ si riduce.
		- ### Strategie
			- **fallimenti casuali**
				- i nodi si rompono casualmente, per cui vengono scelti con la **stessa probabilità**
			- **attacchi**
				- gli ((631cb57b-95f1-4f96-bde0-7c6e6c74e8e7)) vengono deliberatamente presi di mira
				- più è grande il ((6422fb58-b14c-4f73-a8ce-c547d160c906)) , maggiore la probabilità di rimuovere un nodo
			- con il primo approccio, viene rimossa una frazione $f$ dei nodi, scelta casualmente
			- con il secondo, si rimuove la frazione $f$ di nodi con il grado più alto, da quello di grado massimo in giù
			- ![image.png](../assets/image_1663063260380_0.png)
				- le reti reali sono robuste contro i fallimenti casuali, ma fragili contro attacchi mirati.
- # Core decomposition #card
  id:: 646166f8-7fe7-4cbc-a061-f5311a8fd698
  card-last-interval:: -1
  card-repeats:: 1
  card-ease-factor:: 2.5
  card-next-schedule:: 2023-05-15T22:00:00.000Z
  card-last-reviewed:: 2023-05-15T01:42:22.478Z
  card-last-score:: 1
	- **Core**: Parte densa della rete, con nodi di grado alto.
	- Procedura per identificare nuclei sempre più densi, rimuovendo nodi di grado progressivamente più alto.
	- Rimuovendo tutti i nodi di grado $k-1$ e inferiore, la porzione della rete rimanente è detta $k$-core
	- ((646167c9-6be2-463c-bd2a-93aef604a2b8))