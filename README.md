# Desarrollo y Distribución de una Aplicación

## Generación del JAR ejecutable

En IntelliJ, una vez dentro del proyecto que queremos exportar como archivo jar, en la parte de la derecha le daremos al símbolo de Maven(que es una m), luego le daremos a `Plugins -> Jar -> jar:jar`. <br>
Hay que tener en cuenta que tiene que estar bien puesto en el archivo pom.xml la clase main del proyecto dentro de la etiqueta <mainClass>. <br><br>
Una vez realizados estos pasos se generara el archivo jar, en mi caso es: <br>
**Hallowen-1.0-SNAPSHOT.jar**

Y se comprobó su correcto funcionamiento mediante:
**java -jar Hallowen-1.0-SNAPSHOT.jar**

### **📸 Captura 1 (Ejecución correcta del archivo jar generado con Maven):**

<img width="1152" height="403" alt="image" src="https://github.com/user-attachments/assets/ac19cc5f-5d3d-4b7f-b1c8-1e23a4da10f7" />

---

## Creación del ejecutable con Launch4j

Se utilizó Launch4j para generar el archivo Hallowen.exe a partir del JAR.

### ⚙ Configuración principal
**Pestaña Basic:<br>**
- Output File: Tendremos que poner la ruta donde queremos que se genere el archivo .exe.<br>
- Jar. Tendremos que poner la ruta en la cuál se encuentra nos archivo .jar.<br>
- Icon: Si queremos ponerle un icono a nuestro .exe.<br>

**Pestaña Header:** <br>
- Header Type: Seleccionar la opción GUI.

**Pestaña JRE:** <br>
- JRE Paths: Tendremos que poner la ubicación de nuestro JDK (en mi caso era el 21).<br>
- Min JRE version: Tendremos que poner la versión mínima del JDK para poder correr el .exe.<br>
- Max JRE version: Tendremos que poner la versión máxima del JDK para poder correr el .exe.<br>

Una vez configurados estos parámetros, le daremos a Build Wrapper (que es el símbolo del engranaje) y ya se nos generaría el archivo .exe.

**Importante:** En el caso de no poder ejecutar el .exe, asegurarse que la versión de su Java este entre la versión 21 y 25, estando esta última no incluida.

### **📸 Captura 2 (Generación correcta de los archivos hechos con Launch4j):**
<img width="772" height="274" alt="image" src="https://github.com/user-attachments/assets/256ab18a-2f0e-4c6f-b391-f191958a44e0" />

---

## Creación del instalador con Inno Setup

Para crear el instalador abriremos la aplicación Inno SetUp Compiler, luego le daremos a `File -> New`, luego de haber hecho esto se nos abrira las distintas pestañas de configuración, en las cuales podremos configurar lo que queramos que aparezca una vez que una persona ejecute nuestro instalador, ya sea los idiomas, dejar seleccionar al usuario donde hacer la instalación, añadirle un icono a nuestro ejecutable etc.<br>
Una vez hecho todo esto, se nos generara el siguiente archivo:<br>
**APlicación Hallowen.exe**

### **📸 Captura 3 (Proceso de instalación de la aplicación generada con Inno SetUp):**
<img width="304" height="146" alt="image" src="https://github.com/user-attachments/assets/77bd345b-9d05-4b84-aea9-21dadf42b54c" />
