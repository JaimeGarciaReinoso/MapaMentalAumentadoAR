#flashcards/dns 
#review2 

- Vamos a ver un ejemplo de cómo se añaden registros en un servidor de DNS.
- Para ello compramos un dominio, por ejemplo *jaimegarciareinoso.es* en cualquier proveedor autorizado (hay varios).
- Cada proveedor de DNS tiene su propio sistema de configuración, normalmente por web. En la siguiente figura se puede ver el sistema de control del que hemos comprado nosotros:
![Panel de Control DNS](03-Figuras/Panel-control-DNS.png)
- En la figura se pueden ver varias entradas almacenadas en **el servidor autorizado del dominio**, cada una de ellas de un tipo ([[Registros de Recurso (RR) en DNS|RR]]) diferente:
	- Los RR A relacionan los nombres de host del campo *Entrada DNS* con las [[Dirección IP|direcciones IP]] del campo *Valor*. Por ejemplo, el host con nombre *www.jaimegarciareinoso.es* tiene como dirección IP la *217.76.142.216*. Como a veces nos olvidamos de poner en el navegador el nombre del equipo, en este caso *www*, también se suele añadir un RR A para el nombre sin esa parte, en este caso *jaimegarciareinoso.es*, asociándole la misma dirección IP. En la siguiente captura vemos parte del contenido del mensaje *response* que envía el servidor local de DNS al cliente que ha solicitado la dirección IP del servidor web [^1] (nótese que la dirección IP coincide con el campo *Valor* del servidor DNS autorizado):
![Captura Wireshark DNS CNAME](03-Figuras/Wireshark-DNS-A.png)
	- Los RR de tipo CNAME *apuntan* a otro nombre de dominio diferente. Esto quiere decir que cuando se pida resolver un nombre de la columna de la izquierda, se responderá con el nombre que hay en el campo *Valor*. Además, en el mensaje *response* se devolverá otro RR de tipo A, con la correspondencia entre el nombre del campo valor y su dirección IP correspondiente, como se puede ver en la siguiente captura:
![Captura Wireshark DNS CNAME](03-Figuras/Wireshark-DNS-CNAME.png)

[^1]: recordemos que en un mensaje *response* se incluye el campo de *Queries* enviado en la solicitud.