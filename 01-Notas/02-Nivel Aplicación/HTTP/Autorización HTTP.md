#flashcards/http 
#review2

- Mecanismo “específico” para identificación de usuarios previa solicitud del servidor.
	- Código de Estado “401 Authorization Required”.
	- Con cabecera “Authenticate”.
- Mensaje de solicitud debe contener “credenciales”.
	- En cabecera “Authorization”.
		- Credenciales: “nombre de usuario” y “clave”.
	- De manera transparente para el usuario.
		- Se teclean una vez, permanecen en caché de la máquina
	- Sin estado.
		- Credenciales en cada solicitud.
	- Con estado.
		- Servidor asocia una “cookie”.