#flashcards/http 
#review2

- Es {{el almacenamiento temporal de [[Páginas web|páginas]] y [[Recurso web|recursos web]] en el cliente, tras recibir la respuesta del servidor}}.
- Permite {{reducir el tiempo de acceso de los navegadores a recursos accedidos recientemente}}.
- Problema: el contenido puede sufrir modificaciones en el lado del servidor, por lo que la copia en la memoria del cliente estaría desactualizada.
	- Solución: crear una nueva _request line_ para las solicitudes, llamada _If-Modified-Since_ (conocida como **Get condicional**)