#flashcards/dns 
#review2 

- Consiste en {{almacenar copias temporales de resoluciones DNS que NO son responsabilidad del sistema en cuestión (entidad DNS)}}.
	- Posiblemente por haber hecho una consulta recursiva.
	- También puede hacerlo el cliente DNS (resolver) de un host.
	- Se guarda en disco duro o en memoria RAM durante un cierto tiempo (el tiempo de almacenamiento es fijado por el [[Servidor DNS autorizado|servidor DNS autorizado]] del equipo según su campo TTL (ver [[Registros de Recurso (RR) en DNS]])).
- Permite reducir los tiempos de respuesta.
	- Si un cliente DNS ha realizado una consulta en el pasado reciente, posiblemente tendrá dicha información, y por lo tanto no será necesario contactar al [[Servidor DNS local|servidor DNS local]]
	- Si un cliente contacta a un [[Servidor DNS local|servidor DNS local]] que tenga en caché la información solicitada, podrá devolverla sin necesidad de contactar a otros servidores DNS.