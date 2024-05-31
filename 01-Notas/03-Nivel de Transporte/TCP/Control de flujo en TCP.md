#flashcards/tcp/fiabilidad 
#review2 

- Objetivo: {{que un emisor no desborde [^1] a un receptor}}.
- Memoria en el receptor.
	- Una entidad reserva cierta cantidad de memoria para almacenar momentáneamente información que le envía la otra entidad en un [[Buffer del emisor en TCP]]
	- Los segmentos almacenados en el [[Buffer del emisor en TCP]] se procesan en orden.
	- La memoria disponible [[Buffer del receptor en TCP]] se notifica en todos los segmentos TCP que envíe la entidad.
		- En el campo [[Ventana de recepción en TCP]] de la cabecera obligatoria de TCP.

[^1]: en este contexto, *desbordar* significa que se reciban más datos de los que se puedan procesar en un determinado tiempo.