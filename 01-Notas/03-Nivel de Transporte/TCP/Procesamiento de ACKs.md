#flashcards/tcp/fiabilidad/temporizadores 
#review2 

- Al recibir un ACK, la entidad TCP que tenga segmentos pendientes de ser confirmados debe:
	- Comparar el valor del [[Número de asentimiento de TCP]] (AN) con la variable interna **BaseEmision**, que almacena {{el [[Número de secuencia de TCP]] más antiguo pendiente de ser confirmado}}
	- Si el AN > BaseEmision esto significa que {{el ACK confirma uno o más segmentos que estaban pendientes de ser confirmados}}. Por lo tanto:
		- Se actualiza el valor de la variable BaseEmision al número de secuencia más antiguo esperando por ser asentido.
		- Si quedan segmentos por confirmar, se actualiza el valor del temporizador ([[Temporizadores en TCP - Cálculo]]) y {{se inicia un nuevo temporizador}} asociado al segmento {{más antiguo pendiente de ser confirmado}}.