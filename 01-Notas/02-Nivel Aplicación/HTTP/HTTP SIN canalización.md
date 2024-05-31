#flashcards/http 
#review2 

- Si hay que descargase dos o más [[Recurso web]] de un mismo servidor, se debe esperar a descargarse uno para pedir el siguiente.
- Si hay que descargarse $N$ recursos de un servidor, todos de igual tamaño y con tiempo de transmisión $X_p$ el tiempo total de descarga [^1] es [^2]:
	- $T_{PSC} = RTT + N\times (RTT+X_p)$

![[Ejemplo_HTML_sin_canalizacion.png]]

[^1]: se asume que el tiempo de transmisión del GET es despreciable.
[^2]: el $RTT=2\times T_{proc}$