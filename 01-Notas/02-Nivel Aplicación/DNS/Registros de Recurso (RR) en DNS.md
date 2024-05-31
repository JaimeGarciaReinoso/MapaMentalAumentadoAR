#flashcards/dns 
#review2 

- Información que se almacena en servidores DNS. Está formado por cuatro campos: *Tipo*, *Nombre*, *Valor*, *TTL*. El *Nombre* y *Valor* dependen del campo *Tipo*:
	- Si *Tipo = A*, entonces *Nombre* es un nombre de host y *Valor* es la dirección IP correspondiente a dicho nombre.
	- Si *Tipo = NS*, entonces *Nombre* es un dominio y *Valor* es el nombre de host de un [[Servidor DNS autorizado|servidor DNS autorizado]] para dicho dominio.
	- Si *Tipo = CNAME* entonces *Valor* es un nombre canónico/completo correspondiente al alias especificado por *Nombre*.
- En las respuestas de DNS ([[Consultas DNS]]) los servidores DNS contactados devuelven cero o más RR (en un formato diferente al almacenado, pero la información es la misma).