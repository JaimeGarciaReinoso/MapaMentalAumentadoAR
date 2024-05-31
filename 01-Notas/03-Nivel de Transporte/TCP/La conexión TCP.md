#flashcards/tcp
#review2 

- TCP es full-duplex
	- Esto significa que {{ambas entidades pueden enviar datos a su entidad par[^1]}}
- En TCP hay flujo de octetos, no de mensajes.
	- Para TCP lo que recibe del nivel de aplicación es una cadena de octetos, y por lo tanto en el receptor el nivel de TCP no tiene la noción de mensajes.
- TCP es un protocolo punto a punto (sólo hay dos entidades conectadas)
	- No permite [[Multicast]] (un equipo envía a un grupo de equipos) ni [[Broadcast]] (un equipo envía al resto de equipos de la red)
- Se necesita establecer una conexión TCP antes de enviar segmentos con datos, para negociar los parámetros de la conexión (ver [[Establecimiento de la conexión en TCP]])
- Una vez la fase de establecimiento de la conexión TCP termina:
	- El proceso Cliente pasa datos a la capa TCP utilizando el {{[[Socket TCP]]}} creado.
	- TCP realiza [[Segmentación]] si fuese necesario, añade [[Cabecera]] TCP a dichos segmentos y genera PDUs
- Una vez se termina el intercambio de datos se debe cerrar la conexión TCP (ver [[Cierre de la conexión TCP]])

![[Buffers_TCP.png]]

[^1]: [[Entidades par]]
[^2]: [[Variables de estado en TCP]]