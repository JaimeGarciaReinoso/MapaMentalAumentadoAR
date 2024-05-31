#flashcards/tcp/fiabilidad/temporizadores 
#review2 

- El valor al que se inicializa un [[Temporizadores en TCP|temporizador en TCP]], o *timeout* se calcula para adaptarse a las condiciones de la red (ver [[RTT]])
- $Timeout=RTT_{estimado} + 4\times RTT_{desv}$, donde
	- $RTT_{estimado}$ es el valor medio de los $RTT$ medidos [^1].
	- $RTT_{desv}$ es la *desviación típica* de los $RTT$ medidos.
- Cuando un temporizador activo vence, se recalcula el timeout como el doble del timeout anterior.

[^1]: cuando se envía un segmento, la entidad TCP emisora inicia un cronómetro, que se detiene cuando se recibe un asentimiento que confirma dicho segmento. Así se pueden obtener muestras de los valores del $RTT$ para diferentes segmentos.