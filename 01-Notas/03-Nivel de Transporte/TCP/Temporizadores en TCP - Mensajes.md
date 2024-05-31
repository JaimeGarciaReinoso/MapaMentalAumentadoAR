#flashcards/tcp/fiabilidad/temporizadores 
#review2 

- Al recibir un mensaje del [[Nivel de aplicación]], TCP lo segmenta ([[Segmentación]]) si es necesario, añade la cabecera TCP correspondiente, y se lo pasa a su [[Nivel de red]] (en el caso del modelo de Internet, al [[Protocolo IP]]).
- Si no hay ningún temporizador activo, {{se inicia un temporizador asociado a dicho segmento}}.