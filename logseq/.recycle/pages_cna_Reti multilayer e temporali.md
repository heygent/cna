tags:: cna

- # Rete multilayer
	- Una rete può avere più layer, ognuno con i suoi nodi e archi.
		- > es: reti di trasporto aereo di compagnie di volo distinte, ognuna con i suoi nodi e archi.
	- **link intralayer**
		- collegano nodi nello stesso layer.
	- **link interlayer**
		- collegano nodi in diversi layer.
	- **reti multiplex**
		- gli insiemi dei nodi nei diversi layer sono identici
		- i link interlayer sono **accoppiamenti** che collegano lo stesso nodo in diversi layer
		- > es: i layer possono rappresentare diversi tipi di relazione in una rete sociale, come amicizia, legami familiari, colleghi, ecc.
- # Rete temporale
	- Rete multiplex in cui i layer rappresentano collegamenti in diversi momenti (snapshot temporali), ad esempio retweet nel corso del tempo.
	- ![image.png](../assets/image_1662651484338_0.png)
- # Reti di reti
	- In generale, ogni layer di una rete può avere i suoi nodi e archi. Questa può essere chiamata una rete di reti (es: la rete elettrica e internet).
	- L'interazione tra reti in diversi layer sono catturate dai link interlayer.
	- > es: le stazioni energetiche comunicano tramite internet, i router sono attivati dalla rete elettrica.
	- **fallimento a cascata**
	  id:: baa0e947-52eb-406a-a2f1-b7edefd384d1
		- tipo di vulnerabilità imprevedibile che sorge nelle reti di reti, dato che un fallimento in una certa rete può causare problemi massicci in un'altra.