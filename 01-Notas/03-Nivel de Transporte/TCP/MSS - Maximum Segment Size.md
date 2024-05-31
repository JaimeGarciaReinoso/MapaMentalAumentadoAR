#flashcards/tcp
#review2 

# MSS
## ¿Qué es?
- {{Cantidad máxima de **datos** que puede transportar un segmento TCP}}
## ¿De qué depende?
- {{Depende de la MTU[^1] y del tamaño de las cabeceras de nivel de red y de transporte: MSS = MTU - cabecera_red - cabecera_transporte}}
## ¿Cuándo se acuerda la MSS de la conexión TCP?
- {{En la fase de establecimiento de conexión, ya que el cliente envía su MSS, luego el servidor contesta con su propio MSS y finalmente ambas entidades calculan el MSS de la conexión como el valor mínimo anunciado por ambos extremos. Cada entidad envía sus respectivos MSS en un campo **opcional** de la cabecera TCP sólo en los dos primeros segmentos (SYN y SYN+ACK)}}

[^1]: [[MTU]]