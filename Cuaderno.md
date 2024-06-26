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
XHTML extiende HTML aplicando funcionalidades de XML, siguiendo las reglas de este como que las etiquetas deben de estar cerradas, bien posicionadas, en minúscula, etc... resultando esto en arma de doble filo, porque nos puede interesar usar un lenguaje restrictivo como es el caso, o querer algo más flexible como lo es HMTl. En general XHTMl es más moderno y compatible con otros metalenguajes y herramientas XML. En cuanto a desventajas, al ser más exigente en todos los sentidos, puede presentar problemas de compatibilidad con sistemas antiguos y también puede crear problemas de integración al ser más complejo. Tampoco está tan extendido como HTML5 y no es tan flexible como he mencionado.
## Estructura de un documento HTML
Los documentos HMTL suelen seguir una misma estructura que consiste en el "Doctype" para definir el tipo de documento, una cabecera que contiene información variada, un cuerpo que alberga el contenido principal del documento y por último las etiquetas propias que permiten definir la estructura y el formato del documento. Estas al igual que se abren (<html>) hay que cerrarlas (</html>) y pueden contener atributos dentro. Más adelante veremos diferentes etiquetas y elementos de bloque que podemos usar para llevar nuestro documento a otro nivel en cuanto a orden y legibilidad.
## Cabecera HTML
Escrito con la etiqueta <head>, dentro de la cabecera podemos encontrar los siguientes elementos que aportan información sobre nuestro documento:
- **Title**: Le da un titulo a nuestra página
- **Meta**: Indica los metadatos del documento ``` <meta charset="UTF-8"> ``` 
- **Style**: Define el estilo
- **Link**: Sirve para enlazar nuestro documento a otro, por ejemeplo a un .css que que le daría formato a nuestro HTML.
- **Script**: Agrega scripts que se ejecutan junto a nuestra página y que pueden aportar diferentes utilidades. Pueden estar escritos en distintos lenguajes, como por ejemplo JavaScript, útil para lograr una página interactiva y dinámica.
## Cuerpo HTML
Se abre con <body>, encontrando dentro del cuerpo el contenido principal de nuestra web y que queremos compartir con el mundo. Podemos encontrar dentro del cuerpo títulos, indices, articulos, etc.. la mayoría de estos elementos definidos con los elementos de bloque que veremos a continuación.
### Elementos de Bloque
Estos elementos ocupan un espacio inamovible y fijo dentro del documento, y se usan para estrcuturar el archivo, dande un "rol" a cada sección del documento. Entre ellos encontramos:
- **El encabezado**: se abre con <header> y sirve principalmente para delimitar el inicio del documento con un título bien en grande haciendo uso de un "h1", para dar a entender de que va a ir la página o simplemente nombrarla.
- **Navegación**: Crea un area de navegación desde la que se puede acceder al resto de secciones del documento. Suele usarse a modo de índice usando listas ordenadas "ol" u desordenadas "ul" con enlaces internos al resto del documento como iba diciendo, haciendo uso de "href" y asignando un "id" que identifique la sección. Se abre con <nav>
- **Main**: Contiene el grueso de la página y el contenido en bruto. Dentro podemos dividir y clasificar su contenido en distintas secciones con "section", pudiendo incluir contenido independiente dentro de ellas con "article". Se abre con <main>.
- **Aside**: Su etiqueta es la misma, y permite abrir una barra lateral con diferentes opciones o contenido adicional.
- **Pie de página**: Se abre con <footer>, y como su propio nombre indica, añade el típico contenido que se añade al final de una página, como el año o el copyright. Este último podemos ponerlo con la entidad ``` &copy; ```.
### Elementos de Linea
Estos elementos solo utilizan el espacio que ocupan, a diferencia de los elementos de bloque. Existen multitud de ellos con un gran abanico de utilidades distintas entre sí:
- **abbr**: Indica abreviaturas.
- **bdi y bdo**: Definen la dirección del texto junto con "dir".
- **cite**: usado para hacer referencias al autor u a otra información relevante.
- **code**: muestra lineas de código de otros lenguajes pero sin que estas se ejecuten, siendo una especie de comentario.
- **data**: asgina un valores al contenido.
- **dfn**: adjunta una definición a un termino, con el fin de hacer que se entienda.
- **Un largo etc.. que no me da tiempo a poner"**
### Listas, tablas y Formularios.
Aunque se encuentran juntas, estas etiquetas cumplen funciones completamente distintas entre si, exactamente las que les dan nombre.
- **Listas**: podemos crear 2 tipos de listas distintas; ordenadas con ```<ol>``` u desordenadas con ```<ul>```. Las primeras son útiles cuando el contenido debe de seguir un orden, y las otras para cuando es irrelevante. Dentro de estas etiquetas los elementos se adjuntan con la etiqueta ```<li>``` para que pasen a formar parte de la lista.
- **Tablas**: A parte de poder definir su tamaño, estilo etc.. con atributos, las tablas se crean de la siguiente manera: Se abren con la etiqueta <table> y podemos designar las cabeceras de las columnas con <thead> poniendo dentro de esta etiqueta cada columna con ```<th>```, y después el cuerpo de la tabla, con ```<tbody>```, que a su vez incluyen las filas con ```<tr>```, y dentro de cada fila el contenido propio de cada columna, incluyendo dentro de ```<tr>``` las etiquetas ```<td>```
- **Formulaios**: Útiles para recabar información y enviarla al propietario de la página, se comienzan con la etiqueta ```<form>```. Para cada campo del formulario vamos a añadir una etiqueta <label> con un atributo "for=""", que apunta al campo del formulario. Esto sirve para darle un titulo al campo y escribir que clase de información hay que introducir. Dentro de los formularios tenemos distintos tipos de <input> que son las etiquetas que permiten escribir el tipo de dato que se va a recopilar, haciendo uso del atributo "type". Tenemos tipos de campos como "email", "password", "text", etc... que sirven para lo dicho. Debemos de incluir dentro del ```<input>``` los atributos "id" para asociarlo con el "for" del label, un "name" para darle nombre y también podemos poner "required" si queremos que el campo sea obligatorio.
### Elementos Multimedia para HTML5
Dentro de nuestros documento HTML podemos agregar contenido multimedia haciendo uso de las sioguientes etiquetas:
- **video**: Sirve para añadir un video que tenegamos almacenado de manera local en nuestro equipo. Para esto debemos de añadir la etiqueta ```source``` con el atributo "src" que contendrá la ubicación del archivo. Es importante ponerlo con la ruta relativa para que se pueda ubicar si cambiamos de dispositivo. Debemos de indicar dentro de source el tipo de archivo con el atributo "type" ```type="video/mp4"```. Podemos agregar controles de repodrucción dentro de la etiqueta principal escribiendo *controls*.
- **audio**: Funciona exactamente igual que con video, salvo que la etiqueta inicial será audio.
- **Videos de YouTube o de otras fuentes**: Para ello haremos uso de la etiqueta iframe con sus respectivos antributos, que permite incrustar contenido multimedia de otras plataformas en nuestra web, haciendo uso los controladores y tecnologías de la página incrustada, como si de una ventana a la aplicación se tratase.
  ``` <iframe width="560" height="315" src="https://www.youtube.com/embed/Video" frameborder="0" allowfullscreen></iframe> ``` Donde "width" y "height" determinan las dimensiones de lo que será el marco del video, "src" el enlace y tipo en cuestión, "frameborder" el tipo de marco, y "allowfullscreen" para crear responsividad y que el reproductor pueda maximizarse para ocupar la pantalla entera.
- **Mapas interactivos**: Consisten en una imagen con puntos precisos que despliegan información o enlaces al pasar sobre ellos y que pueden contar con distintos factores de forma. Para lograr esto subimos una imagen con la etiqueta scr con dentro el atributo "src" y la ruta relativa de la imagen, además de el atributo "usemap="nombredelmapa" para indicarle la imagen que mapa va a usar. Ahora escribiremos la etiqueta map, donde dentro agregaremos etiquetas area, que definirán los puntos de interés en el mapa. Entre los atributos de esta destacan; "shape" para seleccionar la forma del punto (rect, poly, circle), "coords" que indican en que coordenadas de la imagen se van a ubicar los puntos, "href" para incluir enlaces y "alt" para nombrar el punto. Debemos de incluir el atributo name="nombredelmapa" dentro de map para que el atributo "usemap" de la imagen lo tenga en cuenta.
## Herramientas de edición y desarrollo web.
Podemos encontrar muchas herramientas con este proposito, desde IDES como Eclipse o Vistual Studio Code hasta programas para crear web estáticas haciendo uso de markdown como Blask o Mkdocs o incluso herramientas como GitHub pages para alojar nuestras páginas y poder visitarlas, pudiendo llegar a adquirir nuestro propio dominio.

# Actividad de cuaderno UD4
## ¿Qué es CSS?
CSS es un lenguaje de marcado indispensable hoy en dia para crear páginas webs bien estructuradas y atractivas. Funciona sobre HTML, aplicandole estilos a los elementos definidos en este. CSS significa Cascade Style Sheets, haciendo referencia a la manera en la que el navegador procesa los estilos para aplicarlos.
## Versiones de CSS
CSS se creó en 1996, por los mismos desarrolladores de HTML y XML, la W3C que a dia de hoy sigue manteniendolo hasta su última versión CSS3. Esta versión lanzada en 2012 se compone de módulos, por lo que no se esperan proximas versiones ya que las nuevas implementaciones y funcionalidades vendrán de esta manera, pudiendo decidir si queremos aplicarlas o no. Sin embargo, la versión anterior CSS2.2 (2011) sigue en pié corrigiendo errores de CSS2 (1998), la cual ya no soporta W3C al igual que la primera versión de 1996 CSS1.
## ¿Como se agrega CSS a un documento HTML?
Podemos agregar CSS a un documento HTML de 3 maneras distintas. 
- La primera de ellas es mediante un documento externo que enlazaremos al HTML con la etiqueta "link" y el atributo "href" que referencia al CSS: ```<link rel=”stylesheet” href=”estilos.css” >```
- La segunda opción es a modo de elemento dentro del HTML con la etiqueta "style" la cual contendrá todo el código CSS: ```<style> h1 {font-family: Lato;} </style>```
- la tercera y última opción es a modo de atributo dentro de un elemento para darle estilo a este. El atributo usado se llama "style" respectivamente. ```<p style="color:lightgreen">Ejemplo</p>```
Los cambios al aplicarse en forma de cascada, se puede definir el peso y prioridad de cada estilo para que se procese como queramos. Si utilizamos la orden "!Important" le daremos la prioridad máxima al archivo, pero si no lo hacemos la prioridad se definirá mediante el origen (procesa después los estilos del nvegador), cuanto más especifico mayor importancia, además de que los ultimos estilos en leerse se procesarán antes en la mayoría de los casos puesto que son los más recientes en haberse escrtio por lo que son los más actuales.
## Selectores CSS 
Los selectores en CSS son aquellas reglas que se utilizan para seleccionar a que partes del HTML queremos aplicar los estilos. Existen los siguientes tipos en base al nivel de agrupación de los componentes del HTML:
- **Universal**: Se le aplica a todos los elementos dentro del documento HTML haciendo uso de "*": ```* {
    font-size: 12;
} ```
- **Tipo**: Los estilos se aplican solo al tipo de elemento seleccionado: ```h1 {font-family: Arial}```
- **Clase**: Los estilos se aplican a las clases designadas mediante el atributo "class" dentro del HTML: ```<p class="prueba">Ejemplo</p>``` Código del CSS para la clase "prueba": ```.prueba {color: blue;}```
- **Identificador**: EStilo aplicado a aquellos elementos con un "ID" específico: HTML ```<section id="id1">``` CSS ```#id1 {color: yellow;}```
- **Atributo**: Se aplica a los tipos de atributos especificados: ```input[type="text"]{padding: 10px 10px;}```
Ademas podemos combinar estos selectores y realizar agrupaciones con ellos:
- **Agrupaciones**: Las reglas se aplicarán a todos estos tipos de elementos o clases: h1,h2,p
- **Combinaciones**: Los cambios se aplicarán únicamente a combianes específicas que tienen que darse para que se apliquen. Es una especie de condición. Podemos encontrar esta serie de combinaciones básicas:
  - Hermanos: Combina a todos los elementos situados en el mismo punto dentro de la jerarquia del documento a partir de el primer elemento. Se crean así "A~B"
  - Hijos: Elementos y aquellos en su interior, se usa ">"
  - Hermanos adyacentes: Funciona al igual que los hermanos, salvo porque solo tiene en cuenta al primero que aparezca tras el elemento seleccionado. Se utliza el signo "+"
  - Descendentes: Combina los elementos que descienden en otros dentro de un contenedor como puede ocurrir en las listas "ul li"
### Pseudoclases
Las pseudoclases son variables de los selectores que hacen que solo se apliquen los cambios a los elementos cuando estos pasen a un estado en concreto. Estas pseudoclases se agregan a los selectores añadiendo un :NombrePseudoclase tras ellos: ```h1:hover{color: orange;}``` Aquí una serie de pseudoclases y sus efectos:
- active: cuando el elemento está activo
- checked: cuando hemos marcado un checkbox o casilla
- disabled: cuando el elemento no está activo
- focus: cuando nos centramos en el elemento
- visited: cuando existe un enlace y ya lo hemos visitado.
### Pseudoelementos
Se tratan de características adicionales de CSS que se aplican a partes específicas de los elementos del HTML si influir realmente en ellos, como puede ser la primera letra o linea, etc... Aquí una breve lista de pseudoelementos:
 - after: se aplican después del elemento
 - before: justo antes del elemento
 - first-letter: primera letra del texto
 - first-line: se aplica a toda la primera linea del texto
 - selection: cuando se selecciona parte del texto.
   La sintáxis es la misma que la de las pseudoclases.
## Tipos de datos y unidades en CSS
Dentro de CSS podemos identificar distintos tipos de datos. Esta clasificación nos permite tener una idea más clara sobre como queremos estilizar nuestro documento según el tipo de dato. Los principales y más comunes son:
- Entero: Se tratan de número sin decimales, que bien pueden ser positivos o negativos
- Número: incluyen decimales
- Dimensión: un número junto a su "medida": deg (grados), s (segundos), px (píxeles)
- Porcentaje: Un número que indica un porcentaje haciendo uso de "%"
- Colores: se pueden indicar los más comunes con su nombre (blue, red) o mediante su identificador rgb, hexadecimal o HSL

 Las unidades también pueden clasificarse como absolutas:
- px: píxeles
- cm: centímetros
- mm: milímetros
- Q: Cuarto de milímetro
- in: pulgadas
- pt puntos (1/72 pulgadas)
- pc: picas (1/16 pulgadas)

O como relativas:
- em: tamaño de la letra del elemento padre
- ex: altura de la fuente del elemento
- ch: anchura de las letras
- rem: tamaño de la letra del elemento raiz o inicial
- lh: Altura de la linea del elemento
- vw: 1% del ancho de ventana gráfica.
- vh: 1% del alto de la ventana gráfica.
- vmin: 1% de la dimensión más pequeña de la ventana gráfica.
- vmax: 1% de la dimensión más grande de la ventana gráfica
## Propiedades CSS
CSS posee una serie de reglas, como todos los lenguajes de marcado, para definir así como se debe de estructurar la hoja de estilos. Algunas de las propiedades que más debemos de tener en cuenta son:
- Modelo de cajas: Se encarga del orden de los marcos y formato del bloque del contenido, como si de una caja por capas se tratase. Sus principales características son:
  - Margen exterior: Zona exterior que rodea el resto de elementos. Se escribe marca con "margin"
  - Margen interior: Se escribe con la propiedad "padding" y constituye el espacio en blanco entre el contenido y el borde
  - Borde: Contiene distintos colores y rellenos sobre el límite del elemento. Propiedad "border"
  - Contorno: "outline", linea dibujada sobre el elemento pero sin invadirlo.
  - Ancho: anchura del elemento, propiedad "width"
  - Alto: alto del elemento, propiedad "height"
- Flex y Grid: son 2 propiedades del display que definen como se mostrarán los elementos. Como "flex" se establecerá como un bloque que fluye en x dirección mediante la propiedad "flex-direction". Mientras tanto, "grid" mostrará los elementos de forma cuadriculada pero en bloque, como si de una tabla se tratase, mediante la propiedad "grid-template-columns" delimitando las dimensiones
- Float y position: Float indica la posición desde la que aparecen los elementos y su respectivo contenido, con la etiqueta "float" y haciendo uso de los valores left (elemento a la izquierda), right (elemento a la derecha), none (no desplaza el elemento), inherit (hereda el float del elemento padre). Si la posición del elemento no está indicada por el contenedor lo haremos con "position".
  - static: valor por defecto
  - relative: posición relativa al elemento
  - absolute: posición absoluta con respecto al resto del documento
  - fixed: sigue el flujo del documento
  - sticky: sigue el flujo normal, pero se puede establecer límites en cuanto a su posición.
- Propiedades de texto: podemos darle formato al texto con las siguientes propiedades:
  - color: color del texto
  - font-family: fuente del texto.
  - font-size: tamaño de la fuente
  - font-weight: grosor de la fuente
  - text-align: alineación del texto: right, center o justify.
  - letter_spacing: espaciado entre caracteres.
- Propiedades de listas: podemos darle propiedades a las listas como cambiar sus viñetas etc... :
  - list-style-type: cambia el icono de la viñeta; circle, square, decimal, etc...
  - list-style-position: establece la posición de las viñetas como dentro o fuera; inside; outside.
  - list-style-image: podemos hacer que las viñetas sean imágenes si aportamos el enlace de estas.
- Diseño adaptativo (Media Queries): Sirven para hacer que el contenido se adapte según el tipo de dispositivo que lo procese de manera automática, adaptandose a la resolución, tamaño de la pantalla, etc... Podemos usar una serie de reglas para adaptar el CSS a las distintas dimensiones del dispositivo, haciendo por ejemplo: ```@media screen and (min-width: 480px) {
 body {
 background-color: lightgreen;
 }
}```

# Actividad de cuaderno UD5
## Sindicación de contenidos en la web
La sindicación de contenidos consiste en la utilización de herramientas que permiten a los usuarios seguir de cerca las últimas noticias de las webs que les interesan sin tener que visitarlas directamente, y a las webs crear estos "canales de difusión" para que los usuarios estén actualizados constantemente y recibir más atención. De cara a la web, estas han de proveer un código que puede estar escrito en distintos lenguajes de marcado, como RSS o Atom, los cuales veremos más adelante. El enlace de este código es el que los usuarios usarán para suscribirse al "boletíin", y que pueden encontrarlo habitualmente en el apartado de las redes sociales de la web al final de esta, insertado sobre el icono del sistema de sindicación utilizado.
## Sindicación de contenidos
Como usuarios, y teniendo en posesión el enlace del que hablabamos, podemos usar distintas aplicaciones web que nos permitan hacer uso de el, y poder seguir las noticias de la página que nos interese, y en caso de ser varias, a mantenerlas organizadas y catalogadas, para tener la información siempre disponible. La mayoría de estas aplicaciones funcionan insertando el enlace o código de la web en ellas, y posteriormente guardándolo y desplegando las noticias como si estuviéramos visitando la página en cuestión. Algunos ejemplos de estos programas son los vistos en clase "Feedly" como aplicación web o "Tiny Tiny RSS" a modo de localhost.
## RSS
Por sus siglas "Really Simple Syndication" se trata de sindicador de contenidos mantenido por la W3C y basado en XML, cuya última versión fue publicada en 2003 y ha seguido en uso hasta ahora. Sus archivos cuentan con la extensión .xml o .rss y destaca por su sencillez a la hora de distribuir los contenidos a través de la web.
### Sinntáxis de RSS
Los documentos en rss comienzan igual que un XML cualquiera, indicando la versión de este y la de RSS (la 2.0). Toda la estructura se forma a través de la etiqueta "channel" seguida de un título (tittle), el link a la página principal (link), una descripción (description), lenguaje (language), etc... Dentro de "channel" podemos crear las distintas entradas independientes, definidas con la etiqueta "item", que en su interior contará con las mismas etiquetas vistas para su propia identificación; link, title, etc... El documento se cierra con la etiqueta "rss" al igual que se abrió cuando indicamos la versión
### Ejemplo de RSS
Usaré como ejemplo los ejercicos hechos en este tema sin ir más lejos:
```
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0">
  <channel>
    <title>Noticias de "Apruebo Porque Sí"</title>
    <link>https://www.aprueboporquesi.com</link>
    <description>Últimas noticias y artículos de interés "Apruebo Porque Sí".</description>
    <language>es</language>
    <item>
      <title>Ofertas de primavera en "Apruebo Porque Sí"</title>
      <link>https://www.aprueboporquesi.com/ofertasprimavera</link>
      <description>E aquí nuestra oferta formativa para primavera 2k24!!</description>
    </item>
  </channel>
</rss>
```
## Atom
Atom también está basado en XML y mantenido por W3C al igual que RSS, cuyos archivos usan la extensión .xml o .atom. Aunque tienen bastantes similitudes, Atom es ligeramente más complejo, lo que lo vuelve más flexible gracias a diversas extensiones que lo personalizan, además de contar con control de versiones, funcionalidades para los metadatos, etc... La última versión de Atom se lanzó en 2005.
### Sinntáxis de Atom
La sintáxis de Atom comienza con la versión de XML, seguido del elemento "feed" junto al atributo que lo enlaza a W3C y desde el que se carga el resto del documento. Dentro de "feed" incluiremos las distintas entradas con "entry", donde cada una incluirá una serie de etiquetas muy parecidas a las de RSS para indicar la información. La descripción en este caso se pone con "summary" y las entradas han de contar con un "id". 
### Ejemplo de Atom
```
<?xml version="1.0" encoding="utf-8"?>
<feed xmlns="http://www.w3.org/2005/Atom">

    
  <entry>
    <title>Ofertas de Primavera en “Apruebo Porque Sí”</title>
    <link href="https://ejemplo.com/ofertasprimavera" />
    <id>https://ejemplo.com/ofertasprimavera</id>
    <updated>2024-04-10T12:00:00Z</updated>
    <summary>E aquí nuestra oferta formativa para primavera 2k24!!</summary>
  </entry>
</feed>
```
## Herramientas de validación de canales de sindicación.
Al igual que XML contaba con validadores como DTD o XML Schema para definir su estructura, y diversas opciones para ver si el documento funcionaba correctamente, los canales de sindicación tienen los suyos propios. El mejor que podemos utilizar para Atom y RSS es el de la misma entidad que los mantiene, el de la W3C. Este validador nos indicará que debemos de corregir para que pueda validarse y funcionar adecuadamente.
## Añadir canales de sindicación a una web
Como hemos comentado anteriormente, la web debe de incorporar el código del sindicador de contenidos para que los usuarios puedan comenzar a usar los canales de difusión. Esto se puede lograr de distintas maneras, aunque las más aceptada es enlazando el documento con el html con la etiqueta "link" dentro de la cabecera. También se puede incluir el enlace dentro de la etiqueta "a" con un "href", usado habitualmente en una foto sobre la que pinchan los usuarios.
## Agregadores de canales
Existen aplicaciones webs que nos ayudan a seguir de cerca los contenidos que nos interesan de diversas fuentes de forma centralizada haciendo uso de los enlaces al código del sindicador de la web. Estas funcionan como un panel, en el que añadimos las canales de difusión como comentábamos, y donde podemos clasificarlos y leerlos desde ahí. Existen soluciones en linea, locales o incluso como extensiones de nuestro navegador.
## Canales de sindicación
Aquí una serie de ejemplos de canales de sindicación:
- Xataca: https://www.xataka.com/index.xml
- El País: https://feeds.elpais.com/mrss-s/pages/ep/site/elpais.com/portada
- National Geographic: https://www.nationalgeographic.com.es/feeds/rss.html

# Actividad de cuaderno UD6
## Introducción a Python 
Python es un lenguaje que ha ganado mucho reconocimiento y que está comiendo terreno hasta el punto de convertirse en uno de los más reconocidos debido a su polivalencia, ideal para escribir aplicaciones web, programas, inteligencias artificiales o para analizar datos.
### Python (definición del lenguaje):
Su sintaxis es bastante sencilla, contando con un gran repertorio de códigos que desempeñan casi cualquier función que podamos necesitar a la hora de programar. Python se ejecuta línea por línea, lo que facilita la detección de errores y permite escribir en unas pocas líneas algo que en otros lenguajes nos ocuparía unas cuantas más. Se puede aplicar a otros programas escritos en otros lenguajes como C o Java, es un lenguaje de alto nivel, orientado a objetos, con soporte de la comunidad y muchos recursos online para aprender a usarlo.
### Variables
Python hace uso de variables para determinar los elementos que serán usados en las operaciones a realizar. Las variables en Python se asignan mediante el símbolo "=". 
### Tipos de datos
Existen muchos tipos de datos en python, con una nomenclatura muy similar a la del resto de lenguajes. Podemos encontrar tipos de datos, alfanuméricos, booleanos, etc... como:
- int: números enteros
- float: números con decimales
- string: cadena de caracteres
- bool: booleano (verdadero, falso)
### Estructuras de control
Se tratan de estructuras que nos permiten programar la lógica del programa, para que actue de cierta forma en x circunstancias. 
- Condicionales: Los ordenes se ejecutan cuando se cumple una condición. Algunas estructuras condicionales son "else" o "if"
- Repetitivas: Se tratan de bucles que repiten una misma acción hasta que se cumple una condición que determina su detención. Las más utilizadas son "while" y "for".
### Listas
Contienen una serie de elementos de cualquier tipo de manera ordenada. Pueden agregarse o retirarse elementos después de crear la lista
### Tuplas
Similares a ls listas, salvo que son "inmutables", es decir, que una vez creadas no se pueden alterar. Utilizadas para almacenar elementos que no variarán con el paso del tiempo
## JSON
### Definición
Se trata de un lenguaje de marcas que antaño servía para representar datos en JavaScript, pero con el paso del tiempo ha recibido tanto contenido por parte de la comunidad que hoy en dia es un lenguaje multipropósito. Su sintaxis es mediante etiquetas de apertura y de cierre. 
### Elementos
Los objetos se definen como clave-valor (la clave define el tipo de elemento y el valor su contenido). Existen varios tipos de elementos en un JSON, como los espacios en blanco, los separadores, etc...
### Tipos de datos simples
### Listas (arrays)
Elementos ordenados que poseen un índice que define su posición
### Objetos
Son conjuntos de subelementos definidos dentro de las etiquetas.
## MongoDB
### Definición del motor de base de datos
MongoDB es una base de datos NoSQL de código abierto diseñada para trabajar con grandes volúmenes de datos no estructurados. En lugar de utilizar tablas y filas como las bases de datos relacionales tradicionales, MongoDB almacena la información en documentos BSON, que es una representación binaria de JSON. Esta forma de almacenamiento permite una mayor flexibilidad y escalabilidad, ya que facilita el manejo de datos heterogéneos, así como el crecimiento horizontal a través de la adición de más servidores.
### Instalación y configuración con Docker
Existen diversas formas de instalar MongoDB, y una de ellas es a través de Docker haciendo uso de una imagen que nos permite levantar una instancia para MongoDB. Lo haremos con el siguiente comando:
```
docker run --name mongodb -p 27017:27017 -d
```
Otra forma es con Docker Compose.
### Pymongo
Pymongo nos permite conectarnos a bases de datos MongoDB para poder operar con ellas. Se trata de un paquete de python.
Usaremos los siguientes comandos para conectarnos:
```
my client = pymongo.MongoClient("dirección de la base de datos")
mydb = myclient["nuestrouser"]
mycol = mydb["packages"]
```
- Insertar: Para insertar elementos en la base se utiliza la función "insert_one()" para un único elemento e "insert_many()" para insertar múltiples documentos.
- Consulta: Las consultas se realizan con "find()", pudiendo recorrer el cursor haciendo un bucle "for".
- Borrar: Se utiliza la función "delete"
- Modificar: se utiliza la función "update"
