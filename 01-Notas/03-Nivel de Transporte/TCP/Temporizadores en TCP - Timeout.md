#flashcards/tcp/fiabilidad/temporizadores 
#review2 

- Al vencer un temporizador, TCP retransmite {{el segmento asociado a dicho temporizador}} que, siguiendo la recomendación del RFC 2988, será el {{más antiguo pendiente de ser confirmado}}.
- Se redefine el tiempo del temporizador como {{el doble del valor del temporizador anterior}}.
- Se inicia un nuevo temporizador asociado al segmento reenviado.