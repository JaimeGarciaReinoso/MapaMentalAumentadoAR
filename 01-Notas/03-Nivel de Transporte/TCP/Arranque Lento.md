#flashcards/tcp/congestion
#review2

- Es uno de los algoritmos de control de congestión en TCP.
- Es el modo en el que se empieza después del establecimiento de [[La conexión TCP]]
- Al empezar en este modo, la [[Ventana de congestión en TCP]] (VC) es de {{1 [[MSS - Maximum Segment Size|MSS]]}}.
- Cuando se recibe un ACK, la *VC* se incrementa en {{la misma cantidad de octetos reconocidos:
	- Si se recibe un ACK que confirma 1 MSS, la VC se incrementa en 1 MSS. En general, si se confirman *n* MSSs, la VC se incrementa en *n* MSSs.}}
- El modo de *Arranque lento* finaliza cuando ocurre cualquier de estos tres eventos:
	- Se cumple que VC=[[Umbral en TCP]]
		- Se pasa al modo [[Evitación de la Congestión]]
	- El [[Temporizadores en TCP|temporizador]] vence.
		- Se asume que existe congestión grave en la red.
		- Se actualiza Umbral = 0.5 (Valor VC cuando vence temporizador)
		- Se actualiza VC = 1
		- Se inicia nuevamente *Arranque lento*
	- Se reciben tres ACKs duplicados.
		- Se asume que existe congestión leve en la red.
		- Se actualiza Umbral = 0.5 (Valor VC cuando vence temporizador)
		- Se actualiza VC = Umbral + 3
		- Se pasa al modo [[Recuperación Rápida]]