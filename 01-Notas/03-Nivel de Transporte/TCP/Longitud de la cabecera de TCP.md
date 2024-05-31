#flashcards/tcp
#review2 

- La cabecera TCP es de longitud {{variable}}, pero siempre un múltiplo de {{32 bits}}.
	- Existe una parte obligatoria y una parte opcional.
- El campo *Data Offset* de la cabecera TCP indica el número de palabras de 32 bits que contiene la cabecera de un segmento determinado.
- El campo *Data Offset* tiene 4 bits, por lo que el número máximo de palabras de 32 bits en la cabecera es de 15. Como la parte obligatoria de la cabecera TCP ocupa 5 palabras de 32 bits, quedan 10 para la parte opcional.

