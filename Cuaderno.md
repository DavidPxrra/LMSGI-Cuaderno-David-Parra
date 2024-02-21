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
- Subelementos: Se alojan dentro de los tipos complejos. Establecen relaciones dentro de los elementos que contiene el tipo complejo:
  ```xs:sequence```: indica una secuencia de elementos obligatorios, y en el mismo orden.
  ```xs:choise```: señala una secuencia de elementos alternativos. Solo debe aparecer uno de ellos.
  ```xs:all```: indica una secuencia de elementos opcionales; no es obligatorio que aparezcan todos en el mismo orden.
- Atributos: Todos los elementos pueden albergar atributos que los definen. Algunos de estos atributos son "type" para el tipo de contenido, "use" para determinar la obligatoriedad, o el más común "name" para signar un nombre que identifique el elemento dentro de XML.
- Restricciones: Permiten aplicar como su propio nombre indica, restricciones de todo tipo a los disntitos elementos y atributos. Este es un ejemplo de su sintáxis, para establecer que el elemento tenga que escribirse de una manera específica:
  ```
  <xs:element name="CIF">
                                <xs:simpleType>
                                    <xs:restriction base="xs:string">
                                        <xs:pattern value="[A-Z]{1}[0-9]{7}"/>
                                    </xs:restriction>
                                </xs:simpleType>
                            </xs:element>
  ```
- Tipos de datos: Hemos hablado de los atributos, pues el atributo "type" nos permite saber cual es el tipo de dato del que se trata el elemento. ```xs:string``` se usa para cadenas de caracteres, ```xs:integer``` para valores numéricos enteros, etc... También hay preestablecidos para otras usos mas complejos, sin tener que hacer uso de restricciones para un formato común pero específico, como puede ser la fecha; ```xs:date```. 
- Comentarios de XMLSchema: Los comentarios en XML Schema tienen el mismo uso que citamos para XML, y que en general se comparte en todo el ámbito de la informática. Los comentarios en XML Schema se escriben entre las etiquetas ```<annotation></annotation>```

# Actividad de cuaderno UD7
## Sistemas de gestión de información:
- Características: Los sistemas de gestión de la información son programas que permiten a las empresas que los utilizan monitorizar los procesos y gestionar la actividad e información de la misma. A la larga optimizan y mejoran la eficiencia. 
- Tipos: Existen distintos tipos de Sistemas de Gestión de Información, podiendo clasificarlos entre locales (alojados en equipos de la empresa y trabajando con ellos únicamente dentro del departamento o edificio) o en la nube (utilizando servicios online pudiendo ser provistos por otra empresa, y pudiendo acceder a ellos desde cualquier equipo con una conexión a la nube). También se pueden clasificar teniendo en cuanta el tipo en sí del sistema gestor, siendo los más conocidos los "ERP", "CRM" o haciendo uso de "Business Intelligence). Veremos cada uno de estos tipos a continuación.
## ERP:
Los ERP (“Enterprise Resource Planning) consisten en un paquete software compuesto por distintas aplicaciones, que en sus totalidad deben de cubrir todas las actividades de la empresa, desde las finanzas hasta la producción. 
- **Características y beneficios:** Su objetivo es el de optimizar la producción y gestión de la empresa, mediante la automatización de las tareas. Los ERP proporcionan todo lo necesario en un mismo entorno, e intagran todas las bases de datos en el mismo programa. Los ERP deben de ser seguros respecto a sus datos, garantizando la integridad de estos, además de ser escalables para adaptarse a las necesidades de la empresa
- **Ejemplos ERP más conocidos:** Dentro de los ERP los hay; genéricos (se utilizan los módulos predefinidos que necesita la empresa), configurables (cuyo núcleo se puede configurar para adaptarse al milímetro a la actividad de la empresa) y a medida (consiste en crear un ERP propio diseñado únicamente para satisfacer a la empresa).
  Algunos ERP muy conocidos y usados hoy en dia son:
  	- **Microsoft Dynamics**
  	- **Odoo**
  	- **SAP**
  	- **SAGE**
## CRM:
Los CRM o "Customer Relationship Management" a diferencia de los ERP, no se aplican sobre la actividad y producción de la empresa, si no en las relaciones con los consumidores. Esto se traduce en un programa que nos permite acceder a información relevante sobre los clientes, como las interacciones que tienen con nosotros, además de permitirnos también la automatización de procesos entre otras funcionalidades.
- **Características y beneficios:** Los CRM tienen como objetivo mejorar la relación con los clientes, permitiendo una atención más personalizada y cercana. Todo esto es posible gracias a la gestión de los contactos, diferenciación de los clientes, canalizar los servicios en un único medio, difusión mediante redes sociales etc... Con la información recaudada de los clientes, se facilita la toma de decisiones, ya que entre esta información se deben de encontrar opiniones, preferencias, reportes o valores relacionados con el número de veces que se ha adquirido un servicio, que en definitiva nos permite saber que funciona y que no. Esto nos permite saber por donde entrar para cerrar ventas o hacia donde enfocar las campañas de marketing, lo que nos conducirá a una mejora constante tanto de la empresa como del servicio o productos que ofrece.
- **Ejemplos CRM más conocidos:**
  	- Oracle Customer Experience
  	- Pipedrive
  	- Salesforce
## BI:
- **Definición y componentes:** "Business Intelligence" se trata de una serie de tecnologías cuyo único objetivo, y que comparten entre sí, es el de facilitar la dirección de una empresa para catapultarla al éxito. En sí "BI" no se trata de un Sistema de Gestión de Información, puesto que no es una plataforma unificada, si no que "BI" hace uso de distintos módulos o componentes indepentientes que nos permiten realizar las mismas tareas que haríamos con un sistema de gestión.
- **ETL:** "Extract, Transform and load" consiste en una serie de procesos que recaban información sobre las actividades diarias de la empresa para después procesarla y obtener datos de valor.
- **Data WareHouse:** Como su propio nombre indica, se trata del almacén de datos de la empresa, al que se puede acudir para consultar los datos que posee para poder hacer una toma de decisiones correcta.
- **OLAP:** " Online Analytical Processing" garantiza la disponibilidad de los datos almacenados en el Data Warehouse, los cuales emplearemos en el siguiente componente. Habitualmente se disponen estos datos como un cubo
- **Data Minining:** Se analizan los datos del Data Warehouse en busca de patrones y comportamientos que nos ayuden a saber cuales son las tendencias de los clientes para poder dirigir la empresa hacia su objetivo.
- **Dashboard:** Se trata de un proceso que habitualmente posee una GUI o interfaz gráfica que nos permite visualizar agrupaciones de los datos que precisemos, pudiendo llegar a tomar acción e interactuar con ellos.

# Actividad de cuaderno UD3
## HTML y su evolución:
La historia de HTML está ligada a la de la World Wide WEb, puesto que es el lenguaje de marcado utilizado desde el comienzo para la creación de páginas web, usadas para compartir documentos e información desde cualquier lugar, independientemente del medio gracias al protocolo de transferencia de hipertexto o "http", que permite acceder al contenido escrito en HTML. Se desarrolló en 1991, siendo el principal descendiente del lenguaje SGML junto con XML. Con el paso del tiempo se han ido liberando diferentes versiones, desde la primera actualización, html 1.1 en 1992, hasta hmtl 5.2 en 2017, agregando nuevas etiquetas, funcionalidades y aplicaciones, etc...
## XHTML diferencias, ventajas y desventajas con respecto a HTML
## Estructura de un documento HTML
## Cabecera HTML
- **Title**
- **Meta**
- **Style**
- **Link**
- **Script**
## Cuerpo HTML
### Elementos de Bloque
### Elementos de Linea
### Listas, tablas y Formularios
### Elementos Multimedia para HTML5
## Herramientas de edición y desarrollo web.
