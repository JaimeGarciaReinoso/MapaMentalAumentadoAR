#flashcards/http 
#review2 

Hay tres escenarios posibles:
1. Cuando un usuario visita por primera vez un sitio web que utiliza cookies, el servidor realiza las siguientes acciones al recibir una solicitud:
	1. Genera un identificador único para el usuario.
	2. Crea una entrada indexada en su base de datos asociada a ese identificador.
	3. Envía una respuesta que contiene la cabecera "Set-Cookie" con el identificador, por ejemplo: `Set-Cookie: 4342` en las respuestas.
2. Cuando el navegador recibe una respuesta que incluye una cookie, ejecuta los siguientes pasos:
	1. Agrega una línea al archivo de cookies que gestiona, incluyendo principalmente el "Nombre del servidor" y el "Identificador" (la cookie).
	2. Posteriormente, en cada solicitud que el usuario realiza para navegar por el sitio web:
	    a. El navegador consulta el archivo de cookies.
	    b. Si existe una cookie para el sitio, extrae el identificador y lo incorpora en la cabecera "Cookie" en las solicitudes, por ejemplo: `Cookie: 4342`.
3. Luego, cada vez que el usuario desea navegar por el sitio web:
	1. El navegador consulta el archivo de cookies.
    2. Si existe una cookie para el sitio, extrae el número de identificación y lo incluye en la cabecera "Cookie" en los mensajes de solicitud, por ejemplo: `Cookie: 4342`.