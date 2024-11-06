#review2 

- El checksum se calcula sobre la [[Pseudo-Cabecera IP]], la [[La cabecera UDP]] (el checksum para el cálculo sería de dos octetos a cero) y los datos del segmento UDP. Se añadirán octetos a cero al final para que la longitud total de la cadena anterior sea múltiplo de dos octetos.
- Para calcular el checksum se realizaría un complemento a uno de 16 bits de la suma complemento a uno de la cadena anterior.