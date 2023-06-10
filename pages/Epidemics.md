tags:: cna
slide:: ![ns09](../assets/ns09.pdf), ![ns10](../assets/ns10.pdf)

- # Modelli di contagio semplici e complessi
	- Si diffondono in modi profondamente molto diversi:
		- idee
		- opinioni
		- comportamenti
		- malattie infettive
	- Il contagio può essere semplice o complesso
		- entrambi i tipi si diffondono da persona a persona
		- con contagio **sociale**:
			- le persone decidono di adottare una nuova idea o innovazione
		- con contagio **biologico**:
			- non è dipendente dalla volontà individuale, e non è osservabile da persona a persona
	- Per malattie infettive, data un'osservabilità non triviale, è meglio adottare **modelli non deterministici**, ovvero basate su *casualità* e *probabilità*.
- # Branching process
	- La forma più semplice di contagio
	- Assunzione: la rete sottostante è un albero (infinito):
		- Paziente 0: **radice**
		- un nodo al livello $n$ (che rappresenta un'*ondata* dell'epidemia) è una persona che incontra altre $k$ persone
		- ogni persona trasmette la malattia con probabilità $\beta$
	- Domanda
		- possiamo predire se e quando la malattia scompare?
	- ((6484bca2-ded3-4ea8-bc2b-3d42bd4b82fa))
	- # $R_0$
		- Se nessun individuo nell'ondata $n$ riesce a trasmettere la malattia ad altri individui, l'infezione sparisce dalle ondate $