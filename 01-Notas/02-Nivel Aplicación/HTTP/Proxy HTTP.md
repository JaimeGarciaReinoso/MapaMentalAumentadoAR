#flashcards/http 
#review2 

- Se sitúa lógicamente {{entre los clientes web a los que se quiere dar servicio y los servidores conectados a Internet}}. En los clientes web se debe configurar la dirección IP del proxy.
	- Para los clientes web, el proxy HTTP actúa como un servidor web normal, mientras que para los servidores HTTP, el proxy es un cliente más.
- Cuando un cliente quiere acceder a un servidor HTTP, envía la solicitud al proxy HTTP que tiene configurado, el cual a su vez envía la solicitud al servidor HTTP en cuestión. Al recibir la respuesta, el proxy almacena la información en su caché local y reenvía la respuesta al cliente web.
	- En el caso en el que el proxy tenga en su memoria caché el [[Recurso web]] solicitado por el cliente, realizará los pasos descritos en [[Caché Web]]. De esta forma, el proxy web funciona como una caché colectiva de todos los clientes web que lo estén utilizando.

![[Ejemplo_HTTP_Proxy.png]]