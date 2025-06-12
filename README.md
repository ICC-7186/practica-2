# Práctica 2: Estructuras de Control y Pruebas Unitarias. 📌

Nombre:

NumCuenta:

En esta práctica se realizarán los pruebas unitarias sencillas para un programa intuitivo haciendo uso de estructuras de control, así como el uso de la herramienta Maven para su ejecución por medio de un archivo `pom.xml`.

## Autores 😊
* **Salvador López Mendoza** - *Titular* - [Correo](slm@ciencias.unam.mx)
* **Gerardo Emiliano Figueroa Sandoval** - *Teoría* - [Emiliano-Fs](https://github.com/Emiliano-FS)
* **Ramsés Antonio López Soto** - *Laboratorio* - [ramseslopez](https://github.com/ramseslopez)
  
## Objetivos 🚀

- Entender por qué el uso de pruebas unitarias es importante para el proceso de desarrolo de software.
- Aprender cómo realizar pruebas unitarias sencillas para el código en proceso.
- Aprender a realizar un archivo `pom.xml` para la gentión de un proyecto de manera sencilla.
- Comprender el uso de las diferentes estructuras de control (secuenciales,condicionles, ciclos y salto) para resolver problemas sencillos.

### Pre-requisitos 📋

- Sistema Operativo Linux (Ubuntu, Debian, Fedora, etc.)
- Git versión 2.43.0
- Java versión 21.0.7
- Perfil de GitHub
- Maven 3.8.7

### Instalación 🔧

- Git

Para instalar la versión más reciente de Git:

```bash
sudo apt-get install git

```
Una vez finaliado, verifica la versión instalada.

```
git -v
```

- Java
  
Instala Java con el siguiente comando:

```
sudo apt-get install openjdk-21-jre
```

Al finalizar, verifica la versión instalada.

```
java --version
```
y también del compilador:

```
javac --version
``` 

- Maven

Para instalar Maven, utliliza el siguiente comando:

```
sudo apt-get install maven
```

Al finalizar, verifica la versión instalada:

```
mvn -v
```

## Recursos 📖

Puedes encontrar más información de los recursos a utilizar en:

- [Maven](https://maven.apache.org/)
- [Explicación](https://eudriscabrera.com/blog/2022/apache-maven-101-explicando-la-magia-detras-de-un-archivo-pom.xml)
- [Estructuras de control](https://puntocomnoesunlenguaje.blogspot.com/2012/04/estructuras-de-control.html)

## Ejercicios ⌨️

Realiza los siguientes ejercicios:

### Manejo de cadenas y números.

Tomando como plantilla la clase `Operaciones` debes de completar el cuerpo de los siguientes métodos:

- suma
- división
- potencia
- esPerfecto
- sumarDigitos
- reversa 
- esPalindromo
- ocurrenciasDe
- decimalABinario

La clase debe de estar guardada en un paquete llamado `operaciones` y no es válido utilizar herramientas que resulvan el problema de forma directa, solo puedes utilizar estructuras de control. Además, debes de generar un archivo de prueba `Practica2` donde se vea el funcionamiento de los métodos implementados.

### Pruebas Unitarias

Debes de implementar un archivo donde enlistes diferentes pruebas unitarias llamado `TestOperaciones` donde probarás que todos los métodos anteriores funcionan de forma correcta.

También debes completar el archivo `pom.xml` de forma correcta pues debe de encargar de ejecutar todo el proyecto.  A continuación se muestra un ejemplo:

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>ejemplo</groupId>
  <artifactId>ejemplo</artifactId>
  <version>ICC</version>
  <packaging>jar</packaging>

  <name>Ejemplo MVN</name>
  <description>
   Ejemplo sencillo del uso de mave y junit
  </description>
 <url>https://classroom.google.com/c/Nzg2NzA1NjU3MzU4</url>
  <organization>
    <name>Ramsés Antonio López Soto</name>
    <url></url>
  </organization>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.release>11</maven.compiler.release>
  </properties>

  <build>
    <plugins>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-enforcer-plugin</artifactId>
        <version>3.0.0-M3</version>
        <executions>
          <execution>
            <id>enforce-maven</id>
            <goals>
              <goal>enforce</goal>
            </goals>
            <configuration>
              <rules>
                <requireMavenVersion>
                  <version>3.1.0</version>
                </requireMavenVersion>
              </rules>
            </configuration>
          </execution>
        </executions>
      </plugin>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <compilerArgument>-Xlint:deprecation</compilerArgument>
          <compilerArgument>-Xlint:unchecked</compilerArgument>
          <debug>true</debug>
          <debuglevel>lines,vars,source</debuglevel>
          <showDeprecation>true</showDeprecation>
          <showWarnings>true</showWarnings>
        </configuration>
      </plugin>

      <plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-jar-plugin</artifactId>
        <version>3.2.0</version>
	<configuration>
	  <archive>
	    <manifest>
	      <mainClass>ejemplo.Main</mainClass>
	    </manifest>
	  </archive>
	</configuration>
      </plugin>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-site-plugin</artifactId>
        <version>3.9.1</version>
      </plugin>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-project-info-reports-plugin</artifactId>
        <version>3.1.1</version>
      </plugin>

    </plugins>

    <finalName>ejemplo-mvn</finalName>
  </build>

  <reporting>
    <plugins>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-javadoc-plugin</artifactId>
        <version>3.2.0</version>
        <configuration>
          <source>11</source>
          <charset>UTF-8</charset>
          <author>false</author>
          <version>false</version>
          <use>true</use>
          <windowtitle>Introducción a Ciencias de la Computación</windowtitle>
          <doctitle><![CDATA[<h1>Introducción a Ciencias de la Computación</h1>]]></doctitle>
        </configuration>
      </plugin>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-report-plugin</artifactId>
        <version>3.0.0-M3</version>
      </plugin>

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-jxr-plugin</artifactId>
        <version>3.0.0</version>
      </plugin>

    </plugins>
  </reporting>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.13.2</version>
    </dependency>
  </dependencies>

</project>
```

La estructua del proyecto debe ser la siguiente:

```
practica-2/
    |_ src/
        |_ main/
        |    |_ java/
        |        |_ operaciones/
        |            |_ Operaciones.java
        |            |_ Practica2.java
        |_ test/
        |    |_ java/
        |        |_ operaciones/
        |            |_ test
        |                |_ TestOperaciones.java
        |_ pom.xml
```

Para poder compilar y ejecutar todos los comandos, debes de ubicarte en la carpeta `practica2/`.

Para compilar, debes usar el siguiente comando:

```
mvn compile
```

Para ejecutar todas las prubas unitarias:

```
mvn test
```

Y para ejecutar el programa principal:

```
mvn install
----
java -jar target/practica1.jar
```

## Intrucciones

* La práctica se entrega de forma individual.
* Debes de clonar el este repositorio con el comando `git clone`, agregar tu nombre en la parte de `Nombre: ` y seguido de tu número de cuenta en `NumCuenta: `.
* El código debe ser legible y el nombre varialbes y métodos debe ser adecuado.
* Sube la solución de la práctica antes de las 23:59 del día de mañana.
* Ningún tipo de copia y/o plagio será tolerado.

## Licencia 📄

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para más detalles.
