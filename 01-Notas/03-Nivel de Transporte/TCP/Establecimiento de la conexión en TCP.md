#flashcards/tcp 
#review2 

- El establecimiento de la conexión TCP se realiza en tres fases
	- Intercambio de **tres segmentos especiales**.
		- Los dos primeros segmentos ({{SYN y SYN+ACK}}) no portan datos de la [[Capa de Aplicación]]. Estos dos segmentos incluyen cabeceras opcionales que se utilizan para negociar el [[MSS - Maximum Segment Size|MSS]].
		- El tercer segmento ({{ACK}}) _puede_ portar datos de la [[Capa de Aplicación]]
	- El establecimiento de la conexión TCP finaliza con el establecimiento de {{las variables de estado[^2] y capacidades en buffers[^1]}} que se utilizarán en la fase de envío de datos.
![[Ejemplo_conexion_TCP.png]]

[^1]: [[Buffer del receptor en TCP]] y [[Buffer del emisor en TCP]] 