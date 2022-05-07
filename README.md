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
de etiqueta (nodos) como lo es HTML. 
XPath es a HTML como las expresiones regules son  a un texto.

Por ejemplo, si queremos extraer el titulo de una pagina web realizamos la siguiente busqueda

//div/span//h1[@class="title"][1]

### Nodos

Un nodo es lo mismo que una etiqueta y su contenido. Un nodo puede contener otros nodos. En otras palabras
Xpath nos permite navegar en los diferentes tipos de profundidad deseados con el fin de extraer información.

### Expresiones

Para empezar a buscar con el lenguaje Xpath empezaremos con la sintaxis de la siguiente expresión.

> $x('')

Y adentro de las comillas simples empezaremos abuscar como lo vimos en la sección anterior

> $x('/') 

Con esta expresión estamos accediendo al documento entero

> $x('//h1/a/text()').map(x=>x.wholeText)

Con esta expresión estamos extrayendo el texto de la cabecera. 

Para acceder a propiedades de un nodo unicamente utilizamos un arroba.

> $x('//div/span//h1[@class="title"][1]') 


## Predicados

Cuando queremos realizar busquedas especificas en los nodos usaremos los predicados.
Los predicados son un tipo de busqueda en el nodo especifico que siempre van entre corchetes []

El predicado más simple es el 1, el cual nos traer el primer elemento de un nodo. El segundo predicado es **last()**
Que nos trae el ultimo elemento de ese nodo.


## Operadores

Los operadores logicos nos ayudan a filtrar mas los nodos y llegar mas profundo a nuestra busqueda.
Cabe aclarar que estos van adentro de los corchetes igual que el predicado.

1. != 
2. and
3. or
4. not()

## Wildcards

Los wildcards o comodinos son una herramienta para la cual se utiliza cuando no sabemos con precisión en donde
se encuentra un nodo o como se llama precesiamente. Es una forma elegante de hacer una busqueda.
Veamos algunos ejemplos:

1. / -> Nos devuelve todo el documento HTML
2. // -> Realiza salto de nodos en todo el documento HTML
3. *(asterisco) -> Nos devuelve todos los nodos dentro de un nodo espesifico.
4. @ se utiliza para especificar un atributo dentro de un nodo. @class, @iterprompt
5. @* Nos devuelve todos los atributos de un nodo.
6. node() a diferencia de * trae no solamente los nodos, sino también todo el contenido.

## In-text Search

Para buscar cadenas de caracteres especificas dentro de un texto.

1. starts-with(.,"texto") Busca,para el nodo actual por eso el punto,  todas las cadenas de caracteres que empiecen por dicho texto.
2. contains(., "texto") Busca, para el nodo actual, todas las cadenas de caracteres que contengan dicho texto.
3. ends-with(., "texto") Busca,para el nodo actual por eso el punto,  todas las cadenas de caracteres que terminen por dicho texto.
4. matches(., regex) Busca, para el nodo actual, mediante expresiones regulares y devuelve todo lo que haga match.

## XPath Axes

Un axis o eje representa una relación contextual del nodo actual y se usa para localizar nodos relativos al nodo actual.

|AxisName | Result|
|---------|--------|
|ancestor | Selects all ancestors (parent, grandparent, etc.) of the current node
|ancestor-or-self | Selects all ancestors (parent, grandparent, etc.) of the current node and the current node itself
|attribute | Selects all attributes of the current node
|child | Selects all children of the current node
|descendant | Selects all descendants (children, grandchildren, etc.) of the current node
|descendant-or-self | Selects all descendants (children, grandchildren, etc.) of the current node and the current node itself
|following | Selects everything in the document after the closing tag of the current node
|following-sibling | Selects all siblings after the current node
|namespace | Selects all namespace nodes of the current node
|parent | Selects the parent of the current node
|preceding | Selects all nodes that appear before the current node in the document, except ancestors, attribute nodes and namespace nodes
|preceding-sibling | Selects all siblings before the current node
|self | Selects the current node

Para realizar este tipo de busquedas utilizamos la siguiente sintaxis

axis::node






















