# Web Scraping With Python Basic


Es una tecnica, que es utilizada por un monton de desarrolladores en todo el mundo, que nos sirve para extraer información de internet. Por ejemplo, de un sitio web.

Veremos el uso de Xpath que es un lenguaje que sirve para apuntar a las partes de un documentos XML.

En este curso utilizaremos Python para realizar web scraping. Nos provee de modulos basicos para realizar esta operación.

## Requests

Es una libreria que nos permite controlar HTTP (protocolos)

##BeatufiulSoup4

Nos sirve información de un archivo HTML.

##Selenium

Herramienta que simula un navegador y poder realizar operaciones basicas como si estuvieras en un navegador.

## Scrapy

Es un framework muy utilizado para realizar web scrapping. Por ejemplo, es utilizado por el Reino Unido para recolectar información constantemente de sus ciudadanos.


## HTTP (Hypertext tranfer protocol)

Es un protocolo, es decir, un conjunto de reglas a partir en la que dos computadoras
se comunican en el internet. Estas dos computadoras tienen un nombre: cliente y servidor.

Hay un cliente que realiza una **petición** y hay un servidor que **responde** a una petición.

## Peticiones

### GET

El método get solicita un representación de un recurso especifico. Las peticiones que usan 
el metodo GET solo deben recuperar datos

### HEAD

El método HEAD pide una respuesta similar al método GET pero sin el cuerpo de la respuesta.

### POST

El método POST se utiliza para enviar una entidad a un recurso en especifico, causando
un cambio en el estado o efectos secundarios en el servidor.

### PUT

El modo PUT reemplaza todas las representaciones actuales del recurso de destino
con la carga útil de la petición.

### DELETE

El método DELETE borra un recurso en especifico.

### OPTIONS

El método OPTIONS es utilizado para describir las opciones de comunicación
para el recurso de destino.

### TRACE

El metodo TRACE realiza un prueba de bucle de retorno de mensaje a lo largo de la ruta 
al recurso de destino

### PATCH

El método PATCH es utilizado para aplicar modificaciones parciales a un recurso.

## RESPUESTAS: Códigos de estado de respuesta HTTP

Los códigos de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud 
HTTP especifica. Las respuestas se agrupan en cinco clases:

1. Respuestas informativas (100 - 199)

2. Respuestas satisfactorias (200 - 299)

3. Redirecciones (300 - 399)

4. Errores de los clientes (400 - 499)

5. Errores de los servidores (500 -599)

Para mas información visitar la página: https://developer.mozilla.org/es/docs/Web/HTTP/Status
Los códigos de estado mas recurrentes son 

* 200 - OK
* 301 - Moved permanently
* 302 - Moven temporarily
* 403 - Forbidden 
* 404 - Not Found
* 500 - Internal Server Error
* 503 - Service Unavailable

## HTTP Headers (Cabeceras)

Las cabeceras HTTP permiten al cliente y al servidor enviar información adicional junto
a una petición o respuesta. Una cabecera de petición esta compuesta por su nombre seguido
de dos puntos  ':' y a continuación su valor. 

Para mas información visitar: https://developer.mozilla.org/es/docs/Web/HTTP/Headers



## HTML (Hypertext Markup Language)

Es el componente más básico de la Web. Define el significado y la estructura del contenido web. Además de HTML, generalmente se utilizan otras tecnologías para describir la apariencia/presentación de una página web (CSS) o la funcionalidad/comportamiento (JavaScript).


## Robots.txt 

Robots.txt es un archivo que existe como forma para decirles a las personas que hacer peticiones, o web scraping que no ingresen tan recurrente o negar la petición a ciertas paginas web del sitio. Para acceder  este archivo de cualquier pagina web
unicamente seguimos el siguiente patrón: **www.pagina_web.com/robots.txt**

## XPath

XPath es XML Path Language, es un lenguaje de patrones de busqueda y extracción que sirve para extraer información de archivos
de etiqueta como lo es HTML. 
XPath es a HTML como las expresiones regules son  a un texto.

Por ejemplo, si queremos extraer el titulo de una pagina web realizamos la siguiente busqueda

//div/span//h1[@class="title"][1]





















