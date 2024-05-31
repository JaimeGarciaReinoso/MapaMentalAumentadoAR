#flashcards/tcp
#review2

- Cabecera TCP
	- Parte obligatoria
		- Longitud total: 20 octetos
		- Campos
			- Puerto origen
			- Puerto destino
			- [[Número de secuencia de TCP]] (SN)
			- [[Número de asentimiento de TCP]] (AN)
			- [[Longitud de la cabecera de TCP]]
			- Flags (1 bit cada uno)
				- [[URG (TCP flag)]]
				- [[ACK (TCP flag)]]
				- [[PSH (TCP flag)]]
				- RST
				- [[SYN (TCP flag)]]
				- [[FIN (TCP flag)]]
			- [[Ventana de recepción en TCP]] (W)
			- [[Checksum en TCP]]
			- Puntero de datos urgentes
	- Parte opcional
		- Longitud: variable, pero 40 octetos como máximo
		- MSS es un campo opcional
			- Se incluye sólo en los dos primeros segmentos de la conexión (SYN y SYN+ACK)
- Datos
	- Se incluye el mensaje (o parte del mensaje) del nivel de aplicación.
	- Su longitud debe ser menor o igual que el MSS de la conexión [[MSS - Maximum Segment Size]]

![[Cabecera_TCP.png]]
