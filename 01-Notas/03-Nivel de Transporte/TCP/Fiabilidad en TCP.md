#flashcards/tcp/fiabilidad 
#review2 

- La fiabilidad en TCP consiste en detectar {{tanto **pérdidas de paquetes** (mediante el [[Número de secuencia de TCP]]) como **errores** [[Detección de errores en TCP]](mediante los [[Checksum en TCP]] de cada segmento), así como la corrección de estos problemas mediante la **retransmisión de los segmentos afectados** ([[Retransmisión en TCP]]).}}
- Para poder detectar las pérdidas de paquetes, los emisores deben identificar cada segmento con un [[Número de secuencia de TCP]] al [[Envío de Segmentos en TCP|enviar segmentos con datos]]. 
- A su vez, los receptores utilizan el [[Número de asentimiento de TCP]] para confirmar la recepción de los segmentos, según la [[Política de generación de ACKs en TCP]]. Estos asentimientos son acumulativos [[Reconocimientos acumulativos]].
- Al recibir segmentos con asentimientos, el receptor debe [[Procesamiento de ACKs|procesar los ACKs]].
	- Una entidad TCP debe almacenar los segmentos que envía en un [[Buffer del emisor en TCP]]
- Ante la pérdida de segmentos, es posible que un emisor no reciba los asentimientos del receptor. Para ello se utilizan los [[Temporizadores en TCP]]. Cuando un temporizador vence, se inicia la [[Retransmisión en TCP]].

- #todo enlazar ejemplos
