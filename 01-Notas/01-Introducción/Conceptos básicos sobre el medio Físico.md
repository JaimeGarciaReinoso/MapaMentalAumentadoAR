#flashcards/intro 
#review2
- Bit: {{porción básica de representación de información en el sistema binario}}
- Señal: {{forma de transmitir un bit o conjunto de bits en un medio de transmisión}}
- Enlace: {{medio de transmisión utilizado para la transmisión de señales entre dispositivos de red}}
- Medio guiado: {{propaga señales sobre un medio sólido: cobre (pares, coaxial), fibra de vidrio (fibra óptica)}}
- Medio no guiado: {{propaga señales sobre un medio no sólido, sin necesidad de conductor: radio, por ejemplo}}
- Tiempo de propagación ($T_{prop}$): {{es el tiempo que transcurre desde que se genera la señal en un transmisor hasta que llega al receptor
	- Tiempo de propagación$=T_{prop} = \frac{distancia}{Vel. propagación} = \frac{d (m)}{s (m/s)}$}}
- Tasa de transmisión ($R$): {{es el número de bits que puede generar como señal una tarjeta de red en un intervalo de tiempo dado. Normalmente se expresa en bits/segundo [bps] o en múltiplos de este, como kilobits/segundo [kbps] (1000 bps), megabits/segundo [Mbps]  ($1\times 10^6$ bps) o gigabits/segundo [Gbps] ($1\times 10^9$ bps).}}
- Tiempo de transmisión ($T_{tx}$): {{es el tiempo que necesita la tarjeta de red de un dispositivo para generar la señal correspondiente a la información que se quiere transmitir.
	- Tiempo de transmisión$=T_{tx}= \frac{n (bits)}{R (bits/seg)}$}} 
- Retardo extremo a extremo ($T_{ee}$): {{es el tiempo necesario desde que se comienza a transmitir hasta que la información llega completamente al destino. En un enlace directo:
	- $T_{ee} = T_{tx} + T_{prop}$ }}
- Probabilidad de error de un paquete ($P_{eb}$): {{es la probabilidad de que al menos un bit de los transmitidos haya llegado al receptor con error:
	- $P_{eb} = 1 - (1-BER)^n$
		- $BER$=Bit Error Rate, o tasa de errores de bit
		- $n$ es el número de bits transmitidos en un paquete.}}