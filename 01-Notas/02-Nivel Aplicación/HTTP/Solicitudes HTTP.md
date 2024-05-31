#flashcards/http 
#review2 

- Mensajes generados por los clientes HTTP a los servidores HTTP para comenzar una transacción.
- La primera línea de los mensajes tipo solicitud se llama _request line_, y está compuesta por tres campos separados por espacios:
	- _Método_ ver más abajo los diferentes métodos que existen.
	- _URL_ del recurso solicitado.
	- _Versión_ del protocolo HTTP.
- Los métodos (solicitudes) más utilizados son:
	- GET: para descargar página/objeto (obtener información)*.
		- Mensaje de solicitud más utilizado.
		- Si es el caso, envío de parámetros conjuntamente con el URL.
	- POST: para descargar objeto (enviar información).*
		- Envío de parámetros/información en el cuerpo del mensaje. P.e, para completar un formulario.
		- Lo que devuelve el servidor depende del contenido enviado.
	- HEAD: similar a GET, pero para descargar sólo el encabezado de la página/objeto.
		- Para supervisión y depuración. P.e, última modificación de un objeto, comprobar enlaces, etc.
	- PUT: para cargar nueva página/objeto.
	- DELETE: para eliminar página/objeto.
	- OPTIONS: para consultar opciones.
		- P.e, propiedades del servidor o de algún recurso.