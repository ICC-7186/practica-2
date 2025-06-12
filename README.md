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

La clase debe de estar guardada en un paquete llamado `operaciones` y no es válido utilizar herramientas que resulvan el problema de forma directa, solo puedes utilizar estructuras de control.

### Pruebas Unitarias

Debes de implementar un archivo donde enlistes diferentes pruebas unitarias donde probarás que todos los métodos anteriores funcionan de forma correcta.

También debes realizar un archivo `pom.xml` que se debe de encargar de ejecutar todo el proyecto.

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
