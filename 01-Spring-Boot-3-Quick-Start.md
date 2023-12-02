
https://start.spring.io/

Seleccionaremos Maven
En las versiones escoger la ultima version y evitar Snapshot porque son alpha/beta

Project Metadata
Group com.luv2code.springboot.demo
artifact mycoolapp
name mycoolapp

Dependencias
Spring Web

Generate


Create REST CONTROLLER
![Descripción de la imagen](https://i.imgur.com/UNaaRIm.png)


![Descripción de la imagen](https://i.imgur.com/J0iN2hE.png)

Spring Framework Overview (Descripcion General de Spring Framework)

Sitio oficial 
https://spring.io/

Objetivos de Spring
1.- Desarrollo ligero con Java POJOs (Plain-Old-Java-Objects)
2.- Promover el acoplamiento flexible (loose coupling) haciendo uso de la Inyeccion de Dependencias (Dependency injection)
3.- Minimizar el codigo Java repetitivo

Panorama General de Spring boot
![Descripción de la imagen](https://i.imgur.com/4Uc9nVv.png)

El tema principal de Spring basicamente gestiona como se crean los Beans

La fábrica para crear beans gestiona las dependencias de los beans.

Basicamente puede leer archivos de configuracion para establecer propiedades y dependencias y ademas el contexto es basicamente el contenedor Spring que guarda los Beans en la memoria

Infraestructura
![Descripción de la imagen](https://i.imgur.com/hrPbUe6.png)

AOP:Aspect Oriented Programming - Agregar funcionalidad a objetos de forma declarativa
- Logging, security, transactions, etc
Basicamente permite crear estos servicios para toda la aplicacion - como registro, seguridad, transacciones, instrumentacion, y luego puedes aplicar estos servicios a tus objetos de forma declarativa por lo tanto no es necesario modificar su codigo para tener soporte para esto.
Simplemente agrega una configuracion en el archivo de configuracion y ese servicio se aplicara a su solicitud

Acceso a datos o integracion
![Descripción de la imagen](https://i.imgur.com/lzJpJ30.png)

Basicamente esto es para comunicarse con la base de datos ya sea con una base de datos no relacional o una base de datos NoSQL
![Descripción de la imagen](https://i.imgur.com/COdqV1I.png)
![Descripción de la imagen](https://i.imgur.com/l2fnFHF.png)
![Descripción de la imagen](https://i.imgur.com/Ma3j0m4.png)
![Descripción de la imagen](https://i.imgur.com/e9d8jHd.png)

Web Layer o Framework MVC
![Descripción de la imagen](https://i.imgur.com/4EZ1wlL.png)

Infraestructure - Instrumentations
![Descripción de la imagen](https://i.imgur.com/4BBO7ZO.png)

Test Layer (Desarrollo basado en pruebas)
![Descripción de la imagen](https://i.imgur.com/C5cEZ1Q.png)

Spring Projects
Modulos Spring adicionales que se construyen sobre el marco central, considerelos simplemente complementos, solo usas lo que necesitas
Spring Cloud, Spring Data
Spring Batch (Procesos por lotes), Spring Security
Spring Web Services, Spring LDAP (Acceser a servidores)
others...

https://spring.io/projects

Que es Maven
Es una herramienta de gestion de proyectos para su aplicacion
El uso as popular de Maven es para la gestion y compilacion de dependencias

Que problemas resuelve Maven
Cuando se esta construyendo un proyecto Java es posible que se necesite archivos adicionales como archivos JAR adicionales como Spring, Hibernate, Commons Logging, JSON, etc...
Un enfoque es descargar esos archivos JAR desde el sitio web de cada proyecto y luego se agregaran esos archivos JAR al path / classpath.

Mi proeyecto sin Maven
![Descripción de la imagen](https://i.imgur.com/AWvLlj4.png)

Solución con Maven
Le dices a Maven: los proyectos con los que estas trabajando (dependencias)
Spring, Hibernate etc...
Maven descargara los archivos JAR de esos proyectos por ti.
Luego Maven pondra esos archivos JAR a disposicion durante la compilacion y el tiempo de ejecucion
Entonces puedes pensar en Maven como si fuera tu comprador personal, simplemente le das una lista de compras, saldra a la ciudad y te comprara todo y te lo trae de vuelta para que puedas usarlo
![Descripción de la imagen](https://i.imgur.com/yGPJsUW.png)

Como funciona Maven detras de escena
![Descripción de la imagen](https://i.imgur.com/Hqy0eTQ.png)

Manejar las dependencias JAR
Maven recuperara una dependencia del proyecto
Tambien cualquier dependencia de soporte
Por ejemplo Spring depende de Commons-logging
Maven hara esto por nosotros automaticamente

Construyendo y Ejecutando
Cuando creas y ejecutas tu app
Maven se encargara de la class y construira el path por usted
Segun el archivo de configuracion Maven agregara los archivos JAR en consecuencia

Relacion entre Spring Boot y Maven
Cuando generas proyectos utilizando Spring Initializr
Se puede generar un proyecto Maven

Viendo las dependencias en el archivo Maven pom.xml

Spring Boot Starters for Maven

Estructura Standar del directorio
Normalmente cuando comienzas un nuevo proyecto
Cada equipo de desarrollo idean su propia estructura de directorios
Y no es ideal para los recien llegados
Y no esta estandarizado
Maven resuelve este problema proporcionando una estructura de directorio estandar
![Descripción de la imagen](https://i.imgur.com/7ulte62.png)
pom.xml = archivo de configuracion de Maven

src/main/java = Tu codigo fuente de Java

src/main/resources = directorio de recursos, archivos de propiedades o archivos de configuracion que utiliza su app

src/main/webapp = Colocas tua archivos JSP, cualquier archivo de configuracion web (imagenes, css, js, etc)

src/test = Directorio de pruebas, aqui es donde colocara el odigo fuente de su unidad de prueba y cualquier propiedad y archivo de configuracion.

target = Directorio de destino para el codigo compilado

![Descripción de la imagen](https://i.imgur.com/rlBrbYA.png)
![Descripción de la imagen](https://i.imgur.com/3uvCz71.png)

Beneficios del directorio de estructura standar
Para los nuevos desarrolladores que se unen a un proyecto
Pueden encontrar facilmente codigo, archivos de propiedades, unit tests, web files etc...
La mayoria de los IDEs han incorporado soporte para Maven
Pueden leer o importar facilmente proyectos Maven

Los proyectos de Maven son protables
Como desarrollador puedes compartir proyectos facilmente entre IDEs

Ventajas adicionales de usar Maven
Gestion de las dependencias
    Maven encontrara los archivos JAR por usted
Construir y ejecutar tus proyectos
    No tendras que preocuparte por la ruta de compilacion o la ruta de clases 
Estructura de directorio Standar

Conceptos clave de Maven
POM File - pom.xml

Coordenadas del Proyecto - Proyect Coordinates
Project Object Model file: POM file (Archivo de Modelo de objetos del proyecto)
Archivo de configuracion para el proyecto (Lista de compras para Maven)
Aqui es donde le decimos a Maven: dependemos de X numero de dependencias, sal y encuentralas para el proyecto. Este archivo pom siempre se encuentra en la raiz del proyecto

Estructura del archivo POM
![Descripción de la imagen](https://i.imgur.com/52tPjqX.png)

Archivo POM simple
![Descripción de la imagen](https://i.imgur.com/oI3TGMt.png)

Coordenadas del Proyecto (Project Coordinates)
Identifican de forma unica un proyecto
Es similar a las coordenadas GPS de tu casa: latitud - longitud
Es basicamente informacion precisa sobre como encontrar tu casa

![Descripción de la imagen](https://i.imgur.com/kS2Biqq.png)
Coordenadas del Proyecto - Elementos
Group ID - Nombre de su empresa
Artifact ID - Nombre del proyecto
Version - Version de lanzamiento especifica
![Descripción de la imagen](https://i.imgur.com/eNtdXxP.png)

Ejemplos de Coordenadas de Proyecto
![Descripción de la imagen](https://i.imgur.com/v8n17Mz.png)

Agregando dependencias
![Descripción de la imagen](https://i.imgur.com/udD0qvL.png)

Para agregar un proyecto de dependencia necesitamos el Group ID, Artifact ID
La version es opcional pero la mejor practica es incluir la version (repetible builds)

![Descripción de la imagen](https://i.imgur.com/AUA4HZy.png)

Como encontrar las coordenadas de las dependencias
1.- Visitar las paginas del proyecto
2.- Visita search.maven.org

![Descripción de la imagen](https://i.imgur.com/TODrPRy.png)






