#flashcards/http 
#review2

- Protocolo para la transferencia de [[Recurso web]].
- Especificado en varias versiones: 
	- HTTPv1.0, especificado en la RF 1945
	- HTTPv1.1, especificado en la RFC 2616.
	- HTTP/2 (HTTPv2.0), especificado en la RFC 7540
	- HTTP/3, especificado en la RFC 9114 (no usa TCP como protocolo de transporte)
- Opera en base al modelo Cliente-Servidor
	- El cliente solicita recursos a un servidor.
	- Al recibir las solicitudes del cliente, el servidor devuelve los recursos.
- Protocolo **sin estado** y **no conectivo**
	- En su funcionamiento básico, el servidor no guarda información de clientes ni de transacciones.
- Protocolo no fiable y no seguro.
	- Si se quiere fiabilidad y/o seguridad, se deben utilizar los servicios de otros protocolos (TCP para fiabilidad y TLS para seguridad, por ejemplo).
- Tipos de conexiones TCP para sesiones HTTP
	- No persistentes. Soluciones utilizadas en HTTPv1.0.
	- [[Conexiones persistentes TCP]]. Soluciones utilizadas en HTTPv1.1 y siguientes.
- Hay dos tipos de [[Mensajes HTTP]]
	- Solicitudes, enviadas por los clientes a los servidores.
	- Respuestas, devueltas por los servidores a los clientes.