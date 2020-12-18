
#INSTRUCCIONES DE INSTALACIÓN Y USO DE DESKTOP#

-----------------------------------------------------
****DESCARGAR EL CODIGO FUENTE DE LA APPLICACION****:
-----------------------------------------------------

Para esto es necesario tener instalado el entorno de desarollo Eclipse. Una vez instalado ir a File -> Import -> Git -> Projects from Git -> Clone Uri -> https://github.com/ams2Proyecto1JAP/Desktop -> Next -> seleccionar solo "pre" -> Next -> seleccionar CloneSubmodule -> Finish.



----------------------------
****CREAR LA BASE DATOS****:
----------------------------

Para esto es necesario tener MySQL Server operativo en el sistema. Entrar en MySQL y crear una base de datos con el comando -> create database "nombre";



----------------------------
****AÑADIR DEPENDENCIAS****:
----------------------------

Es necesario añadir las dependencias de JSON y de lipeRMI para poder ejecutar el proyecto, para ello es necesario tenerlas descargadas en el sistema con los siguientes links: 

lipermi-0.4.jar --> https://sourceforge.net/projects/lipermi/files/lipermi/lipermi-0.4/lipermi-0.4.jar/download
json20200518.jar --> https://jar-download.com/artifacts/org.json/json/20200518/source-code --> Click en "Download json (20200518)"

Una vez tengas ambas dependencias en local, desde Eclipse hacer click derecho en el proyecto Duolingo_Desktop --> Build Path --> Configure Build Path --> Libraries --> Classpath --> sustituir las rutas de los .jar haciendo doble click en ellos y seleccionando el lugar donde estén en tu sistema



-----------------------------------------------------
****PASOS PREVIOS ANTES DE LANZAR LA APPLICACION****:
-----------------------------------------------------

En el explorador de archivos de eclipse ir al proyecto lib -> (carpeta) src/main/java -> (paquete) duolingo.lib.hibernate.util -> (Archivo) "HibernateUtil.java" --> Abrir el archivo y hacer la siguientes modificaciones:

linea 25, [enlace base de datos]: sustituir con tus datos ip, puerto y nombreBaseDatos en "jdbc:mysql://ip:puerto/nombreBaseDatos?serverTimezone=UTC"

linea 26, [usuario]: sustituir "user" en settings.put(Environment.USER, "user"); con el nombre de tu usuario de la base datos.

linea 27, [password]: sustituir "password" en settings.put(Environment.PASS, "password"); con tu password de la base datos.

LANZAR LA APPLICACION:

En el explorador de archivos de eclipse ir a Duolingo_Desktop -> src -> main -> Interface.java. Abrir el archvio y ejecutar el programa (Run Interface). La aplicacion esta lista para usarse.
