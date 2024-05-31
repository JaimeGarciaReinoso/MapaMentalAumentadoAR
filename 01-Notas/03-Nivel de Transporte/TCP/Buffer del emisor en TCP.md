#flashcards/tcp/fiabilidad 
#review2 

- Una entidad TCP debe almacenar los segmentos enviados en una memoria temporal, o buffer del emisor. 
- Tan pronto se reciba confirmación de la correcta recepción del segmento, la entidad TCP puede eliminar el segmento de su buffer de emisor.
- En el caso de ser necesaria la [[Retransmisión en TCP|retransmisión]] de un segmento, este se obtiene del buffer del emisor.