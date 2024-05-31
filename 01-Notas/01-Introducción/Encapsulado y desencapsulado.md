#flashcards/intro 
#review2 

- En la comunicación vertical de un [[Host]] transmisor , una capa superior (en el nivel *i+1*) envía una ([[Unidad de datos del protocolo (PDU)|PDU]]) a la capa adyacente inferior (en el nivel *i*), junto con información de control ([[Interfaz de información de control (ICI)|ICI]]). La capa inferior, añade una {{[[Cabecera|cabecera]]}} a la PDU recibida (que en este nivel llamaremos {{[[Unidad de datos del servicio (SDU)|SDU]]}}) y genera su propia PDU de nivel *i*. Se dice que esta capa *i* *encapsula* [^1] la PDU recibida.
- En la comunicación vertical de un [[Host]] receptor, una capa inferior de nivel *i+1* recibe su PDU del nivel inferior. Esta capa *i+1*, extrae y procesa la cabecera de su nivel que contiene la PDU recibida. Si todo es correcto, elimina esa cabecera (lo que se conoce como {{desencapsulado}}) y envía el resto del contenido a la capa superior *i*, que recibirá la PDU de nivel *i*.

![[Modelo-de-capas.png]]

[^1]: podemos utilizar el símil de una cápsula de café, en donde la cápsula envuelve o protege el café que tiene en su interior. En nuestro caso, la cabecera de nivel *i* "protege" la PDU de nivel *i+1*.