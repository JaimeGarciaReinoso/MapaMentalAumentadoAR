#flashcards/http 
#review2 

- Si hay que descargase dos o más [[Recurso web]] de un mismo servidor, se pueden enviar todas las solicitudes {{en secuencia sin necesidad de esperar sus respuestas}}.
- Si hay que descargarse $N$ recursos de un servidor, todos de igual tamaño y con tiempo de transmisión $X_p$ el tiempo total de descarga[^1] es [^2]
	- $T_{PCC} = 2\times T_{prop} + N\times X_p$

![[Ejemplo_HTML_con_canalizacion.png]]

[^1]: se asume que el tiempo de transmisión del GET es despreciable.
[^2]: uno de los $T_{prop}$ es debido a la propagación del GET y el otro a la propagación del objeto (se ve claramente en la figura como el último bit del último recurso necesita un $T_{prop}$ para llegar al cliente.)