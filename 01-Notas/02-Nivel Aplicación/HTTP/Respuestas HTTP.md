#flashcards/http 
#review2 

- Mensajes generados por el servidor como respuesta a la solicitud de un cliente.
- La primera línea de los mensajes de tipo respuesta se llama _status line_, y está compuesto por tres campos separados por espacios:
	- _Versión_ del protocolo HTTP.
	- _código de estado_ ver más abajo.
	- _phrase_ es una descripción, en texto, del código de estado.
- Los _códigos de estado_ representan las posibles respuestas que puede devolver un servidor. Es un valor de tres caracteres numéricos, en donde el primero indica el **tipo** de código, que pueden ser estos:
	- **1xx**: información, respuesta provisional.
	- **2xx**: éxito en la resolución de la solicitud.
	- **3xx**: redirigir solicitud, necesarias más acciones.
	- **4xx**: error del cliente.
	- **5xx**: error del servidor.
- Algunos de los códigos más utilizados son:
	- 200 (phrase: OK). 
	- 201 (phase: Created)
	- 301 (phrase: Moved permanently)
	- 401 (phrase: Unauthorized)
	- 404 (phrase: Not Found)