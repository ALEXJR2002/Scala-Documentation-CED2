# Instalación Scala para IntelliJ


## Introducción

Primero que todo, debemos tener previamente instalado el [JDK 8](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)  o [JDK 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) de Java. Estas versiones nos evitarán errores en el proceso de instalación. Además, requerimos también el archivo de instalación de [Scala](https://github.com/coursier/launchers/raw/master/cs-x86_64-pc-win32.zip) [^bignote], el cual asegura que tengamos instalados todas las herramientas y comandos necesarios en nuestro sistema para usar el lenguaje propiamente. 


## Creando el proyecto
1. Abre IntelliJ y selecciona “Nuevo proyecto”
![image](https://user-images.githubusercontent.com/72985018/176945653-b30a4ffa-ea6f-49c5-b423-d84717b7d7fb.png)

    - Si no está instalado el plugin de Scala, lo instalamos dando click en "+" y seleccionamos "Scala"
    ![image](https://user-images.githubusercontent.com/72985018/176946962-1d8509e5-7432-42ca-93d9-11d55748ffc7.png)

    - Luego procedemos dando click en "Instalar" y reiniciamos el IDE
    ![image](https://user-images.githubusercontent.com/72985018/176947086-c1ad32b8-be59-4c41-9206-5edf4cbb1670.png)

2. En "Build System" seleccionamos "sbt" y dejamos todo como está. Nombramos el proyecto como queramos, en este caso lo llamaremos "SbtExampleProject". Finalmente, procedemos a crear.
![image](https://user-images.githubusercontent.com/72985018/176948092-43a88267-7f22-4271-a382-408a94343b8c.png)

## Entendiendo la estructura del proyecto
sbt crea diversos directorios que pueden ser útiles cuando se empiecen a crear proyectos más complejos. Por ahora se pueden ignorar la mayoría de ellos pero aquí está un rápido vistazo a cada uno de ellos:

  - .idea (Archivos de IntelliJ)
  - project (plugins ajustes adicionales para sbt)
  - src (archivos source o principales)
      - main (código de la aplicación)
          - java (Archivos principales de Java)
          - scala (Archivos principales de Scala) <-- Es todo lo que necesitamos por ahora
      - test (Pruebas Unitarias)
  - target (Archivos generados)
  - build.sbt (Archivos de definición de la build para sbt)

## Más información
Para investigar más profundamente sobre Scala en IntelliJ puedes revisar [Building a Scala Project with IntelliJ and sbt](https://docs.scala-lang.org/getting-started/intellij-track/building-a-scala-project-with-intellij-and-sbt.html) donde podrás revisar a detalle el proceso de codificación y creación de proyectos en IntelliJ.

[^bignote]: El instalador puede solicitar [vcruntime140.dll](https://www.dll-files.com/vcruntime140.dll.html)  y [vcruntime140_1.dll](https://www.dll-files.com/vcruntime140_1.dll.html). Descargar estos archivos en la ruta C:\Windows\System32 de modo que el instalador los reconozca. 

    En caso de no solicitarlos, ignorar estos archivos.



