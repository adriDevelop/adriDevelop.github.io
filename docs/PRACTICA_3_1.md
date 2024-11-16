# Práctica 3.1: Instalación de Tomcat y Maven para el despliegue de una aplicación Java.

Esta práctica consiste en realizar la instalaciñon del servidor Tomcat en una máquina nueva. Así que, lo primero que haremos, será crear una máquina nueva de debian.

Una vez la tengamos, procederemos con la instalación de Tomcat.

### Instalación de Tomcat

Para comenzar con la práctica, nos hará falta tener java instalado. Para ello, ejecutaremos el siguiente comando:

```sudo apt install defaulr-jre```
![alt text](<./imagenes_actividad_3_1/Captura de pantalla 2024-11-16 a las 11.52.26.png>)

Una vez instalado, instalaremos Tomcat.
```sudo apt install tomcat10 tomcat10-admin```

![alt text](./imagenes_actividad_3_1/image.png)

Y comprobaremos los puertos que tenemos disponibles mediante 

```ss -ltn```
![alt text](./imagenes_actividad_3_1/image-1.png)

### Añadir usuarios a nuestro Tomcat.

Para poder manejar nuestro tomcat, deberemos de tener un usuario capaz de realizar las acciones. Para ello, vamos a crearnos un usuario desde el archivo donde se almacenan los usuarios de tomcat, editando el archivo de configuración.

```sudo nano /etc/tomcat10/tomcat-users.xml```
![alt text](./imagenes_actividad_3_1/image-2.png)

Una vez dentro, deberemos de añadir la siguiente línea de código en el archivo.
![alt text](./imagenes_actividad_3_1/image-3.png)

Reiniciamos nuestro servicio de Tomcat y comprobamos que se encuentre funcionando correctamente.

```sudo systemctl restart tomcat10```
```sudo systemctl status tomcat10```
![alt text](./imagenes_actividad_3_1/image-4.png)

Y accedemos a localhost:8080/manager/html y comprobaremos que nos pide el logueo del usuario con el nombre de usuario y su contraseña.
![alt text](./imagenes_actividad_3_1/image-5.png)

Y nos debería de aparecer la siguiente pantalla.

![alt text](./imagenes_actividad_3_1/image-6.png)

Con esto, ya tendríamos Tomcat funcionando correctamente en nuestra máquina. Podríamos comprobarlo accediendo al ejemplo que nos aparece en la página.

![alt text](./imagenes_actividad_3_1/image-7.png)

Si queremos trabajar con otro .war, deberemos de añadirlo. (El ejemplo de la documentación de moodle no funcionaba, aquí el error).

![alt text](./imagenes_actividad_3_1/image-8.png)

Entonces he decidido trabajaremos con otro .war que funcione correctamente el cual mostraré mas adelante en la práctica. Ahora procederé con la instalación de maven.

### Instalación de Maven
Deberemos de instalar maven para hacer los despliegues.
Para ello haremos uso del siguiente comando.

```sudo apt install maven```
![alt text](./imagenes_actividad_3_1/image-9.png)

Comprobaremos que se ha instalado correcramente mediante el comando

```mvn --v```
![alt text](./imagenes_actividad_3_1/image-10.png)

Ahora deberemos de configurar un usuario para hacer uso de los scripts.

![alt text](./imagenes_actividad_3_1/image-11.png)

### Clonación del repositorio que haremos uso.
Ahora, como dije anteriormente, haremos uso de un .war externo. Para ello haremos la clonación del repositorio del que haremos uso.

![alt text](./imagenes_actividad_3_1/image-13.png)

Antes de hacer el despliegue, deberemos de configurar el despliegue desde el pom.xml para que contenga la ruta a la que queremos desplegar la aplicación.

![alt text](./imagenes_actividad_3_1/image-14.png)

Una vez configurado, accedemos dentro de la carpeta del directorio que hemos clonado y ejecutamos el comando

```mvn tomcat7:deploy```
![alt text](./imagenes_actividad_3_1/image-15.png)

Y nos deberá de mostrar la siguiente salida de que se ha realizado correctamente.

![alt text](./imagenes_actividad_3_1/image-16.png)

Y si accedemos a la página de localhost:8080/manager/html, deberemos de ver la aplicación desplegada.

![alt text](./imagenes_actividad_3_1/image-17.png)

Y ahí la tendríamos con nombre pipedrapapeltijeras que fue la ruta que especificamos cuando modificamos nuestro pom.xml.

Ahora accederemos y haremos unas pruebas. Básicamente es un piedra papel o tijeras en el que nosotros cogemos una opción y la máquina coge otra y devuelve si ganas o pierdes y un contador.

![alt text](./imagenes_actividad_3_1/image-18.png)









