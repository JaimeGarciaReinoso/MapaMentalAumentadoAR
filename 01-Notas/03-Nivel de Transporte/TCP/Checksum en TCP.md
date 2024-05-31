#flashcards/tcp 
#review2 

- Mecanismo empleado en TCP para {{detectar posibles errores durante la transmisión}}.
- El emisor calcula el checksum, que es función del contenido del segmento TCP a transmitir y de la pseudo-cabecera IP[^1], para luego incluirlo en el campo correspondiente de la cabecera TCP. El receptor comprueba si el valor incluido en el campo checksum coincide con sus propios cálculos de dicho valor.

[^1]: la pseudo-cabecera IP incluye las direcciones IP origen y destino, la longitud del segmento TCP y el protocolo de transporte, así como una secuencia fija de ceros. Esta pseudo-cabecera sólo se utiliza para calcular el checksum, pero **no se transmite**.