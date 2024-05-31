#flashcards/intro 
#review2 

- Debido a la [[MTU]] que impone el nivel de enlace, el resto de niveles superiores deben limitar el tamaño de sus propias [[Unidad de datos del protocolo (PDU)|PDU]]: 
	- La PDU que genere el nivel de red debe ser, como mucho, la [[MTU]], por lo que:
		- $Tamaño(PDU_{red}) = Tamaño(Header_{red}) + Tamaño(SDU_{red}) = Tamaño(Header_{red}) + Tamaño(PDU_{transporte}) \leq MTU$
		- $Tamaño(PDU_{transporte}) \leq MTU - Tamaño(Header_{red})$
	- Por otro lado, la PDU de transporte se genera con la SDU de nivel de aplicación a la que se concatena la cabecera de transporte, por lo que:
		- $Tamaño(PDU_{transporte}) = Tamaño(Header_{transporte}) + Tamaño(SDU_{aplicacion}) \leq MTU - Tamaño(Header_{red})$
		- $Tamaño(SDU_{aplicacion}) \leq MTU - Tamaño(Header_{red}) - Tamaño(Header_{transporte})$
- En algunos casos, el nivel de transporte ofrece el servicio de *segmentación* al nivel de aplicación, lo que implica que este último nivel puede enviar mensajes de cualquier longitud, y es el nivel de transporte el que *segmenta* o divide el mensaje en trozos que cumplan la última inecuación.
- Por lo tanto, la segmentación es {{el proceso que realiza el nivel de transporte de segmentar los mensajes de nivel de aplicación para garantizar que se cumple el tamaño máximo de trama impuesto por la [[MTU]].}}