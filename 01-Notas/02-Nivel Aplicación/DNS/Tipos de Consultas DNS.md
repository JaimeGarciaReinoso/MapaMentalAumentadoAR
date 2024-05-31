#flashcards/dns 
#review2 

- Locales
	- - Se utiliza para consultas a la [[Caché DNS]] local.
- Recursivas [^1]
	- Servicio por el cual un servidor DNS contacta con otros servidores DNS en el caso de no tener la información solicitada en una consulta.
- Iterativas [^1]
	- Servicio por el cual un servidor DNS responde con el registro de otro servidor DNS más apropiado. Esto se hace cuando el servidor contactado no tiene la respuesta exacta para la consulta recibida.
- Inversas
	- Es una consulta en donde se solicita un nombre de host dada una dirección IP.

[^1]: **Normalmente**, los [[Servidor DNS local]] ofrecen un servicio recursivo, mientras que el resto de servidores ([[Servidor DNS raíz]], [[Servidor DNS TLD]] y [[Servidor DNS autorizado]]) ofrecen un servicio iterativo.