#flashcards/http 
#review2 

El formato de mensajes HTTP es similar para *solicitudes* y para *respuestas*
- Cabeceras, compuesta por:
	- *Request line* (en caso de [[Solicitudes HTTP]]) o *status line* en caso de [[Respuestas HTTP]].
	- *Header lines* aportan infomación extra. Una por línea. Tienen el formato:
		- header field name: \<sp\> value \<cr\>\<lf\>
		- El *header field name* es el nombre concreto de la cabecera utilizada y *value* contiene el valor de dicha cabecera.
- *Cuerpo*:
	- Opcional en los mensajes de solicitud. Cuando se incluye, contiene parámetros relativos al recurso solicitado.
	- En los mensajes de respuesta contiene:
		- Recurso solicitado, en caso de éxito.
		- Texto relativo a un error, en caso de haber un problema.

![[Formato_solicitudes.png]]
![[Formato_respuestas.png]]