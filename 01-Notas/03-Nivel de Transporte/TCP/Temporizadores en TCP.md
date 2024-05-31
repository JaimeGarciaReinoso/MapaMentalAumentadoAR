#flashcards/tcp/fiabilidad/temporizadores
#review2 

- La gestión de los temporizadores requiere muchos recursos, por lo que para TCP, el [RFC 2988](https://datatracker.ietf.org/doc/html/rfc2988) **recomienda**
	- Un único temporizador de retransmisión, independientemente del número de segmentos pendientes de ser confirmados.
- Sucesos importantes en el emisor TCP, relativos a la transmisión y retransmisión de datos, son:
	- Mensajes recibidos desde una aplicación ([[Temporizadores en TCP - Mensajes]])
	- Fin de temporización ([[Temporizadores en TCP - Timeout]])
	- Recepción de ACK nuevo ([[Procesamiento de ACKs]])