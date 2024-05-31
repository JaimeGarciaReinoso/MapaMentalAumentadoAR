#flashcards/tcp/congestion 
#review2 

- Es un modo recomendado, no obligatorio, aunque actualmente la mayoría de las implementaciones lo incluyen.
- En este modo se intenta recuperar lo antes posible la pérdida de un segmento.
- La VC se incrementa {{en un MSS por cada ACK duplicado recibido}}.
- Cuando se recibe el ACK para el segmento que falta, entonces:
	- VC = Umbral
	- Umbral = 0.5 (Valor VC cuando vence el temporizador)
	- Se pasa al modo [[Evitación de la Congestión]]
- Cuando vence el temporizador
	- Umbral = 0.5 (Valor VC cuando vence el temporizador)
	- Se establece VC = 1 MSS.
	- Se pasa al modo [[Arranque Lento]]