# Desarrollo y Distribución de una Aplicación

## Generación del JAR ejecutable

En IntelliJ, una vez dentro del proyecto que queremos exportar como archivo jar, en la parte de la derecha le daremos al símbolo de Maven(que es una m), luego le daremos a Plugins -> Jar -> jar:jar. Hay que tener en cuenta que tiene que estar bien puesto en el archivo pom.xml la clase main del proyecto dentro de la etiqueta <mainClass>.
Una vez realizados estos pasos se generara el archivo jar, en mi caso es:

**Hallowen-1.0-SNAPSHOT.jar**

Y se comprobó su correcto funcionamiento mediante:

java -jar Hallowen-1.0-SNAPSHOT.jar

<img width="1152" height="403" alt="image" src="https://github.com/user-attachments/assets/ac19cc5f-5d3d-4b7f-b1c8-1e23a4da10f7" />

## Creación del ejecutable con Launch4j

Se utilizó Launch4j para generar el archivo Hallowen.exe a partir del JAR.

⚙ Configuración principal
Pestaña Basic:
Output File: Tendremos que poner la ruta donde queremos que se genere el archivo .exe.
Jar. Tendremos que poner la ruta en la cuál se encuentra nos archivo .jar.
Icon: Si queremos ponerle un icono a nuestro .exe.

Pestaña Header:
Hedaer Type: Seleccionar la opción GUI.

Pestaña JRE:
JRE Paths: Tendremos que poner la ubicación de nuestro JDK (en mi caso era el 21).
Min JRE version: Tendremos que poner la versión mínima del JDK para poder correr el .exe.
Max JRE version: Tendremos que poner la versión máxima del JDK para poder correr el .exe.

Una vez configurados estos parámetros, le daremos a Build Wrapper (que es el símbolo del engranaje) y ya se nos generaría el archivo .exe.

📸 Captura 3:
Carpeta HallowenDistribucion con el exe, jar y carpeta jre.

4️⃣ Creación del instalador con Inno Setup

Se creó un instalador Windows que copia la aplicación, crea accesos directos y permite la desinstalación completa.

Archivo generado:

HallowenInstaller.exe


Funciones verificadas:

Instalación correcta.

Acceso directo en escritorio y menú inicio.

Desinstalación sin dejar restos.

📸 Captura 4:
Pantalla inicial del instalador.

📸 Captura 5:
Aplicación instalada ejecutándose desde el acceso directo.

📸 Captura 6:
Pantalla de desinstalación finalizada.
