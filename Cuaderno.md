# Cuaderno
## Tabla de contenidos.
## Enlaces de interes
[w3, aprender programación](https://www.w3.org/)


# Actividad de cuaderno UD1
## Qué es un Lenguaje de marcas
Los lenguajes de marcas son aquellos utilizados para hacer las estructuras de datos que se muestran a la hora de visitar una web o visualizar un documento, haciendo uso de etiquetas o marcas que le dan formato. Estas etiquetas le añaden un valor adicional al texto, ya que indican cualidades; si se trata de un título, un párrafo, etc...
## Evolución de los Lenguaje de marcas
Los lenguajes de marcas, al igual que las demás tecnologías del software, han ido evolucionando a lo largo de los años, con mejoras en la depuración del código, nuevas funciones e implementaciones, mayor rendimiento, etc... A continuación veremos un par de antecesores de XML para conocer un pelín más sobre la historia de los lenguajes de marcado.
- SGML: Por sus siglas "Standard Generalized Markup Language" se trata de un lenguaje de marcado que data de 1986 y de el estándar a la hora de estructurar un documento electrónico, sin tener en cuenta el método y herramienas que se utilizan. Más adelante se extendió a HTML y XML para solventar distintos errores.
- GML: De este lenguaje surge el ya visto SGML. El "Generalized Markup Languaje" se creo en 1969 por IBM con la premisa de unificar los lenguajes de marcas para evitar posibles errores a la hora de convertir archivos. No debe de confundirse con el "Lenguje de Marcado Geográfico" el cual es una derivación de XML utilizado para estrcuturar, transportar y almacenar información geográfica que surgió en 2007. Este permite el uso de primitivas como geometrías, topologías, unidades de medida, coordenadas, direcciones, etc...
## Características de los lenguajes de marcas
Los lenguajes de marcas suelen ser facil de utilizar y de interpretar. Hacen uso de etiquetas. Su lenguaje es estático. Se despliegan rápidamente. Multiplataforma. En lenguajes como XML, el contenido esta separado del formato, por lo tanto se puede remodelar facilmente sin dañar el contenido. Son texto plano. Lenguaje flexible, compacto y facil de procesar.
## Características y ejemplos de los siguientes lenguajes de marcas:
- XML: Permite crear etiquetas y esquemas. Diseño y contenido independiente. Formato texto. Guardado e intercambio de datos flexible. Una única raiz.
  Ejemplo:
```
  <pizzas>
<pizza nombre="Barbacoa" precio="8">
<ingrediente nombre="Salsa Barbacoa"/>
<ingrediente nombre="Mozzarella"/>
<ingrediente nombre="Pollo"/>
<ingrediente nombre="Bacon"/>
<ingrediente nombre="Ternera"/>
</pizza>
  
```
- HTML: Diseñado para su visualización en navegador. Numerosos estilos gracias a CSS. Junto a lenguajes como JavaScript permite crear aplicaciones web.
  Ejemplo:
```
 <html>
	<head>
		<title>
			Ejemplo
		</title>
	</head>
	<body>
  <h1>Ejemplo</h1>
  </body>
 </html>
 ```
- JSON: lenguaje usado para representar objetos de JavaScript. Consiste en pares "clave-valor". Ligero y facil de exportar. Permite la anidación de otros objetos.
  Ejemplo:
```
  {
    "v": 1,
    "title": "Hola mundo",
    "date": "2023-06-06T08:53:03.090Z",
    "autor": "davidparra",
    "type": "mejemplo"
}
```
  - YAML: Diseñado para ser facil de comprender y de intercambiar información con el. Funciona usando tabulaciones para tabular los datos. Utilizado para estructurar archivos de configuración.
  Ejemplo:
```
  --

Acerca de: m>

 Hola, soy David

 De Almería y me gusta

 escuchar deathcore melódico
```
## XML: definición y características del metalenguaje
- prologo: Se trata de las primeras lineas del codigo que indican la versión y el tipo de documento ente otros datos que pueden resultar relevantes sobre todo a la hora de exportar el documento.
- Contenido: Es el contenido en sí del archivo, al cual el resto de elmentos como etiquetas deben de darle formato. Pueden ser un conjunto de datos que aportan información sobre otro.
- atributos: utilizados para diferenciar elementos con el mismo nombre.
- Ejemplos en XML
  ```
  <?xml version="1.0" encoding="UTF-8" standalone="no"?>
	<root>
		<clients>
			<client DNI="73061632 Q">
				<name> Melquiades </name>
				<lastname1> Ojeda </lastname1>
				<lastname2> Targaryen </lastname2>
			</client>
		</clients>
		
		<products>
			<product fechainicio="12/02/2022" fechafin="26/12/2023">
				<name> Botijo Carmesí </name>
			</product>
			<product fechainicio="05/11/2019" fechafin="16/10/2023">
				<name> Manatí MKII </name>
			</product>
		</products>
	</root>
  ```
# Actividad de cuaderno UD2
## Documentos XML; estructura:
- Declaración o prólogo: se trata de un elemento opcional que se escribe al comienzo del archivo XML, en el que se indican datos relevantes como la versión de XML o si se trata de un archivo
  único o si está enlazado a algún archivo externo, como bien podría ser un DTD para su validación. Aquí un ejemplo para ver su sintáxis, la cual no suele variar mucho:
  ```
  <?xml version="1.0" encoding="UTF-8"?>
  ```
- Elementos: Los elementos componen el grueso de un archivo XML, indicando los datos y de que clase son, albergando en su interior otros elementos para crear estructuras complejas de información.
  Los elementos siempre tienen una etiqueta que los abre y otra que los cierra, y siempre debe de haber un elemento raiz que englobe a todos los demás que conformen el fichero. Los elementos dentro de otros
  elementos se llaman hijos, y los que los albergan, padres. Los elementos se componen habitualmente de caracteres alfanuméricos.
  ```
  <prueba>esto es una prueba</prueba>
- Atributos: Se escriben entre comillas y dentro de la etiqueta de apertura de un elemento. Se utilizan para aportar información extra y definir aun más un fichero XML. Poseen sus propias reglas como comenzar por una letra o "_" o que diferencian entre mayúsculas y minúsculas etc... Ejemplo:
  ```
  <elementaco nombre="cebolla"></elementaco>
  <!-- cebolla es el atributo, y esto es un comentario, el cual veremos que es en el siguiente apartado -->
  ```
- Comentarios: Los comentarios a la hora de la verdad, no aportan nada a la funcionalidad o disposición del XML, si no que sirven como anotaciones para guiar a las personas que utilizan dichos archivos. Pueden aclarar la finalidad del archivo, incluir peticiones, reglas o metodologías que han de cumplirse para escribir el código como es debido, también pueden tener un propósito didactico, de advertencia, entre un millón de utilidades que se le pueden atribuir. Se escriben así:
  ```
  <!-- Esto es un pedazo de comentario -->
  ```
- Espacios de nombres: Los espacios de nombres son usados para definir el tipo de dialecto XML por así decirlo, que va a usarse en el fichero, con la finalidad de resolver posibles problemas que surjan a causa de la existencia de elementos o atributos que se repitan. Se escriben como un atributo específico seguido de una URL.
```
  xmlns:xs="http://www.w3.org/2001/XMLSchema-instance"
<!-- Se escriben dentro de la etiqueta de apertura (como cualquier otro atributo) del elemento raiz -->
```
- Entidades: Estas permiten añadir informarción que ya está definida en el mismo DTD del documento, o proporcionada de forma externa por el espacio de nombre. Pueden ser aplicables para un único archivo para el que están escritas o externas, que se pueden aplicar y mantienen sus valores fuera de este. Existen 5 entidades por defecto, y esta es una de ellas:
  ```
  &apos;
  ```
- CDATA: Todo lo que se incluyan dentro de la sección CDATA será texto plano el cual no será procesado, pero que si formará parte del documento, a diferencia de un comentario.
  ```
  <![CDATA[ aqui podría ir cualquier cosa, como otro fragmento de codigo de ejemplo]]>
## Validación de documentos:
### DTD:
- Entidades:
- Anotaciones:
- Elementos:
- Atributos
### XMLSchema:
- Definición:
- Estructura básica:
- Elementos locales y globales:
- Elementos simples:
- Elementos complejos:
- Subelementos:
- Atributos:
- Restricciones
- Tipos de datos:
- Comentarios de XMLSchema
