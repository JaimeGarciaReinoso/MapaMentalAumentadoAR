#review2

- Ejemplos utilizando la figura 1 que se puede ver más abajo.
	- Cuando se transmite el segmento con SN=1 se activa un temporizador asociado a dicho segmento. Cuando se recibe el segmento con AN=11, que confirma la recepción del segmento transmitido anteriormente, se desactiva el temporizador del segmento con SN=1.
	- Cuando se transmite el segmento con SN=11 se activa un temporizador, asociado a dicho segmento, ya que no existe ningún temporizador activo. Al transmitirse el segmento con SN=21, no se activa ningún temporizador para dicho segmento [^1]. Cuando se recibe el asentimiento que confirma los dos segmentos enviados anteriormente, se desactiva el temporizador activo, asociado al SN=11.

Figura 1:
![[Ejemplo_Temporizadores_1.png]]

- Ejemplos utilizando la figura 2 que se puede ver más abajo.
	- Cuando se transmite el segmento con SN=31, se activa un temporizador asociado a dicho segmento. Los segmentos con SN 41, 51 y 61 no generan nuevos temporizadores, ya que en el momento de su transmisión ya hay un temporizador activo.
	- Al recibir el AN=51 en el host A, se detecta que se confirma el segmento al que está asociado el temporizador activo. Por lo tanto, se desactiva el temporizador activo. Además, y como los segmentos SN=51 y SN=61 están aún pendiente de confirmación, se activa un nuevo temporizador asociado al más antiguo de ellos, es decir, para el SN=51.
	- Cuando se recibe el AN=71, se desactiva el temporizador activo, ya que se confirma el segmento asociado a dicho temporizador. Como no hay ningún segmento pendiente de ser confirmado, no se activa ningún temporizador.
	- Al enviar el segmento con SN=71, se activa un temporizador para dicho segmento. Como dicho segmento se pierde, el host B al recibir el SN=81 (fuera de secuencia) envía un ACK duplicado con AN=71.
	- Ya que un sólo ACK duplicado no genera ningún evento, el temporizador asociado al segmento SN=71 vence, por lo que se envía otra vez el segmento SN=71. El host B envía un ACK con AN=91, que al llegar al host A, desactiva el temporizador activo.

Figura 2:
![[Ejemplo_Temporizadores_2.png]]

[^1]: se asume que sólo puede haber un temporizador activo, como se recomienda en el RFC 2988 [[Temporizadores en TCP]]