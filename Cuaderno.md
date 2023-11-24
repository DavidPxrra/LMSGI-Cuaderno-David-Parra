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
### DTD: Lo componen una serie de reglas que permiten validar documentos XML. Puede formar parte del documento o validar este de un archivo externo. La estrcutura de DTD se basa en la de XML, por lo que si queremos añader restricciones mas complejas podemos optar por otro dialecto de validación mas completo como XML Schema.
- Entidades: Ya hemos hablado de las entidades en la estructura de XML, y estas pueden estar definidas por ejemplo dentro del DTD para establecer valores dentro del documento que valide este DTD, como ya habíamos dicho, al igual que pueden ser internas o agenas al archivo.
  ```
  <!ENTITY nombreEntidad “valor”>
  ```
- Anotaciones: Las anotaciones nos permiten saber si una entidad es no XML y su formato, y que por lo tanto no ha de ser procesada. Pueden ser públicas o privadas.
  ```
  <!NOTATION nombre SYSTEM “URI”>
  ```
- Elementos: Los elementos DTD no tienen mucho misterio; definen la estrucutra de los elementos XML que representan. Pueden declarar que un elemento es obligatorio (#REQUIRED) entre muchos otros parámetros que podemos poner dentro del elemento. Su sintaxis es la siguiente:
  ```
  <!ELEMENT ejemplo (#REQUIRED)>
  ```
- Atributos: Actuan al igual que los elementos. Podemos aplicarle un sin fin de configuraciones modificando el tipo de, atributo, si es obligatorio o no, etc...
  ```
  <!ATTLIST producto ref CDATA #REQUIRED>
  ```
### XMLSchema:
- Definición: XML Schema al igual que DTD nos permite realizar la validación de XML pero de una forma mucho más compleja y detallada basada en la utilización de etiquetas, escribiendose como XML pero con sus propias reglas.
- Estructura básica: La estructura básica de XML Schema es la siguiente:
```
  <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="peliculas">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="pelicula">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="titulo"></xs:element>
                            <xs:element name="director"></xs:element>
                            <xs:element name="sinopsis"></xs:element>
                            <xs:element name="actores">
                                <xs:complexType>
                                    <xs:sequence>
                                        <xs:element name="actor" maxOccurs="unbounded"></xs:element>
                                    </xs:sequence>
                                </xs:complexType>
                            </xs:element>
                            <xs:element name="estreno" type="xs:date"></xs:element>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>
```
Se escribe como hemos dicho haciendo uso de etiquetas, englobandose todas dentro de ```<xs:schema>```. Los elementos poseen tipos simples o complejos, que definen que clase de elementos, restricciones o atributos engloban, los cuales veremos detalladamente a continuación
- Elementos locales y globales: Los elementos locales son hijos de un elemento que no seal el raiz, los cuales son de un solo uso, mientras que los elementos globales son hijos del raiz y pueden ser reutalizados. Un ejemplo del global seria cada alumno dentro de un elemento raiz llamado alumnos, mientras que cada elemento dentro de cada alumno, como bien podría ser clase,asgintaruas, etc.. conformarían los elementos locales. Los eleemntos poseen etiqueta de apertura y cierre como todo lo demás dentro de XML Schema y se representarían así: ```<xs:element name="ejemplo"></xs:element>```
- Elementos simples: Son aquellos que guardan información directamente, como un texto, valor, etc... Hacen uso del atributo "type" para autodefinirse o utilizan restricciones.
  ```
  <xs:element name="minima">
                                <xs:simpleType>
                                    <xs:restriction base="xs:integer">
                                            <xs:minExclusive value="-50"></xs:minExclusive>
                                    </xs:restriction>
                                </xs:simpleType>
                            </xs:element>
  ```
- Elementos complejos: Son aquellos que alojan otros elementos, que pueden ser simples o complejos a su vez. También pueden aplicar restricciones a las relaciones entre elementos.
  ```
  <xs:element name="actores">
                                <xs:complexType>
                                    <xs:sequence>
                                        <xs:element name="actor" maxOccurs="unbounded"></xs:element>
                                    </xs:sequence>
                                </xs:complexType>
                            </xs:element>
  ```
- Subelementos:
- Atributos:
- Restricciones
- Tipos de datos:
- Comentarios de XMLSchema
