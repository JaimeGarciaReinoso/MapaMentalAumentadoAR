#flashcards/http 
#review2 

- Mecanismo HTTP que {{permite que el cliente pregunte al servidor si la copia que tiene almacenada (que descargó con anterioridad) es válida}}.
	- En las [[Respuestas HTTP]], el servidor incluye, además del recurso web, la fecha de última modificación del objeto (_request_line_ _Last-modified_), por lo que el cliente, además de guardar el objeto en su caché, incluye también esta fecha.
	- Antes de enviar una [[Solicitudes HTTP|solicitud HTTP]], el navegador comprueba si ya tiene el contenido en su caché. Si es así, añade la _request line_ **If-Modified-Since** junto con la fecha de última modificación almacenada junto al recurso.
- Al recibir una solicitud que incluya la cabecera **If-Modified-Since**, un servidor comparará la fecha de modificación local con el valor que acompaña a la cabecera:
	- Si las fechas coinciden (objeto no modificado), el servidor contestará con una respuesta {{con código _304 (Not modified)_ y con el **cuerpo del mensaje vacío**}}
	- Si las fechas no coinciden (objeto modificado) el servidor contestará con un mensaje {{con código _200 (OK)_ y el cuerpo del mensaje contendrá el [[Recurso web]] solicitado.}}
		- Además, la cabecera **Last-modified** contendrá la fecha y hora de última actualización del objeto.
		- Al recibir este mensaje, el cliente web actualizará su caché.