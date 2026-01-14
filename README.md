# Desarrollo y Distribución de una Aplicación

## Generación del JAR ejecutable

En IntelliJ, una vez dentro del proyecto que queremos exportar como archivo jar, en la parte de la derecha le daremos al símbolo de Maven(que es una m), luego le daremos a Plugins -> Jar -> jar:jar. Hay que tener en cuenta que tiene que estar bien puesto en el archivo pom.xml la clase main del proyecto dentro de la etiqueta <mainClass>.
Una vez realizados estos pasos se generara el archivo jar, en mi caso es:

**Hallowen-1.0-SNAPSHOT.jar**

Y se comprobó su correcto funcionamiento mediante:

java -jar Hallowen-1.0-SNAPSHOT.jar



3️⃣ Creación del ejecutable con Launch4j

Se utilizó Launch4j para generar el archivo Hallowen.exe a partir del JAR.

⚙ Configuración principal
Opción	Valor
Output file	Hallowen.exe
Jar	Hallowen-1.0-SNAPSHOT-shaded.jar
Header type	GUI
Bundled JRE path	jre
Min JRE version	21
Max JRE version	25

La JRE fue incluida dentro del proyecto para permitir la ejecución en equipos sin Java.

📁 Estructura final
HallowenDistribucion/
 ├─ Hallowen.exe
 ├─ Hallowen-1.0-SNAPSHOT-shaded.jar
 └─ jre/
       ├─ bin/
       └─ lib/


📸 Captura 2:
Ventana de configuración de Launch4j.

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
