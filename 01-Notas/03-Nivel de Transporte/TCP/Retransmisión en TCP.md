#flashcards/tcp/fiabilidad 

- Un emisor debe almacenar en su [[Buffer del emisor en TCP]] los segmentos que ha enviado.
- Ante el vencimiento de un [[Temporizadores en TCP|temporizador]] o al entrar en el modo de [[Recuperación Rápida]], el emisor debe reenviar el segmento más antiguo pendiente de confirmación.
