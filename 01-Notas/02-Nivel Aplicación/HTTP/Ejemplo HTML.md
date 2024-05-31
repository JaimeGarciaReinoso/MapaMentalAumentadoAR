#flashcards/http 
#review2


- Este es un ejemplo simple de un fichero [[HTML]]
>\<!DOCTYPE html\>
>
>\<html\>
>
>\<head\>
>  \<title\>Ejemplo HTML Básico\</title\>
>\</head\>
>
>\<body\>
>  \<h1\>Encabezado de nivel 1\</h1\>
>  \<p\>Este es un párrafo de texto.\</p\>
>  \<h2\>Encabezado de nivel 2\</h2\>
>  \<p\>Otro párrafo de texto. \</p\>
>  \<a href="https://www.ejemplo.com/hola.html"\>¡Página de bienvenida!\</a\>
>  \<img src=”https://www.ejemplo.com/imagen.jpg" alt=”Imagen"\>
>\</body\>
>
>\</html\>

- Si un navegador procesa este fichero, la salida sería la siguiente:
	- **IMPORTANTE**: después de procesar el fichero HTML visto al principio, el agente de usuario del navegador detecta que debe descargarse el [[Recurso web]] con [[Direccionamiento en HTTP|URL]] https://www.ejemplo.com/imagen.jpg. Una vez descargada dicha imagen, el agente de usuario ya puede mostrar la página web completamente.
	- Si el usuario hace click en el enlace, el agente de usuario deberá pedirle al cliente HTTP del navegador que se descargue el objeto con la URL asociada.

![[Ejemplo_basico_HTML.png]]

- 
