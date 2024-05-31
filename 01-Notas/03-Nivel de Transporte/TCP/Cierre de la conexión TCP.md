#flashcards/tcp 
#review2 

- Una vez se ha terminado el intercambio de datos, cualquiera de las dos entidades (digamos, la A) inicia el cierre de la conexión TCP enviando un segmento con los flags FIN y ACK a 1. La otra entidad debe enviar un segmento de confirmación con el ACK a 1. Posteriormente, la entidad B debe enviar otro segmento con los flags FIN y ACK a 1, a lo que responde A con un segmento con el flag ACK a 1.
- Una vez cerrada la conexión, ambas entidades liberan todos los recursos asignados a la conexión ([[Buffer del emisor en TCP]], [[Buffer del receptor en TCP]], etc.)

![[Ejemplo_cierre_conexion_TCP.png]]