#flashcards/dns 
#review2 

- El formato de solicitudes y respuestas del protocolo DNS es el mismo, y se puede ver más abajo:
- Sección cabecera son los 12 primeros bytes, y contiene los siguientes campos:
	- Identificador (2 bytes) asignado por el cliente y devuelto sin cambio en la respuesta, para relacionar las solicitudes con sus respuestas.
	- Indicadores (2 bytes) dispone de varios subcampos o flags:
		- Flag de Consulta (0) o Respuesta (1)
		- Flag de Autorización: indica si el servidor DNS que responde es autorizado (1) o no.
		- Flag de "Solicitud de Rercursión" indica, en una *solicitud* que el servidor DNS realice recursión (1) si no dispone del RR.
		- Flag de "Recursión Disponible" indica, en una *respuesta*, si el servidor DNS admite (1) o no (0) recursión.
	- Campos "Número de ..." indica, cada uno de ellos, el número de campos de capa tipo que siguen después de la cabecera.
	- Campo Cuestiones contiene información acerca de la consulta.
	- Campo Respuestas contiene los registros del recurso solicitado, que pueden ser varios.
	- Campo Autoridad contiene registros de otros [[Servidor DNS autorizado|servidores DNS autorizados]].

![[Mensaje_DNS.png]]