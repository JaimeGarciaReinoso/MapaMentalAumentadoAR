#flashcards/tcp/congestion 
#review2 

- Modo de control de congestión de TCP en donde se incrementa la [[Ventana de congestión en TCP]] de forma lineal.
- La [[Ventana de congestión en TCP]] (VC) se incrementa en {{una unidad cuando se reciben VC asentimientos.
	- Ejemplo: si la VC es de 10 MSS [^1] se podrán enviar 10 segmentos de MSS octetos. Cuando se reciba el ACK que confirma el décimo segmento, la VC pasará a ser de 11.}}
- Por lo tanto, el VC se incrementa en $MSS/VC$ cada vez que se recibe el ACK de un segmento [^1].
- El modo de Evitación de la Congestión finaliza cuando se cumple cualquiera de estos dos eventos:
	-  El [[Temporizadores en TCP|temporizador]] vence.
		- Se asume que existe congestión grave en la red.
		- Se actualiza Umbral = 0.5 (Valor VC cuando vence temporizador)
		- Se actualiza VC = 1
		- Se pasa al modo de [[Arranque Lento]]
	- Se reciben tres ACKs duplicados.
		- Se asume que existe congestión leve en la red.
		- Se actualiza Umbral = 0.5 (Valor VC cuando vence temporizador)
		- Se actualiza VC = Umbral + 3
		- Se pasa al modo [[Recuperación Rápida]]

[^1]: en el RFC se utiliza la VC anterior y no el valor entero de la misma como hacemos nosotros para simplificar el cálculo.