#flashcards/http 
#review2 


- Algunas _header lines_ que son comunes a los mensajes de *solicitud* y *respuesta*: 

| **Cabecera** | **Contenido** |
| --- | --- |
| Date | Fecha y hora en que se envía el mensaje |
| Connection | Indica en relación con la conexión TCP, cerrar o mantener |

- Algunas _header lines_ de mensajes de _solicitud_:
 
| **Cabecera**| **Contenido** |
| --- | --- |
|Accept|Tipos de Contenidos que el Cliente puede aceptar|
|Accept-Charset|Conjunto de caracteres que el Cliente puede aceptar|
|Accept-Encoding|Codificaciones que el Cliente puede aceptar|
|Accept-Language|Idiomas que el Cliente puede manejar|
|Host|Nombre de dominio del Servidor|
|Authorization|Credenciales del Cliente (nombre de usuario y clave)|
|Cookie|Notificación de “cookie”, previamente establecida por un Servidor|

- Algunas _header lines_ de mensajes de _respuesta_:
  
|**Cabecera**|**Contenido**|
| --- | --- | 
|Server|Información del Servidor|
|Content-Encoding*|Tipo de codificación del contenido|
|Content-Language|Idioma utilizado por el público al que va destinado el contenido|
|Content-Length*|Nº de octetos del contenido|
|Content-Type*|Tipo MIME del contenido|
|Last-Modified|Fecha y hora de la última modificación del recurso|
|Location|Indica al Cliente dónde enviar solicitud para el recurso solicitado|
|Set-Cookie|Cookie que el Servidor envía al Cliente|
|Authenticate|Indicación al Cliente que se requiere autenticación|