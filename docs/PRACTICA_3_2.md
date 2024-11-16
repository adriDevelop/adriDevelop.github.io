# Practica 3-2. Instalacion de Node.js Express y test de la primera aplicación.

Para empezar con esta práctica, debemos de parar nuestro servicio de Tomcat ya que nos podría ocasionar problemas. Para ello:

```sudo systemctl stop tomcat10```
![alt text](./imagenes_actividad_3_2/image.png)

Una vez realizado, procedemos a instalar mediante el siguiente comando.

```sudo apt -y install nodejs npm```

Cuando lo tengamos instalado, deberemos de instalar tambien Express. Para ello haremos uso del siguiente comando:

```sudo npm install -g express```
![alt text](./imagenes_actividad_3_2/image-1.png)

Ahora, una vez que hayamos terminado de instalar todo lo necesario, procedemos con el despliegue de nuestra apliación.

### Despliegue de aplicación de manera local.

Empezaremos clonando nuestro repositorio, del cual haremos el despliegue. 
```git clone https://github.com/MehedilslamRipon/Shopping-Cart-Application```
![alt text](./imagenes_actividad_3_2/image-2.png)

Y accederemos a la carpeta.

```cd Shopping-Cart-Application```

Una vez dentro, debemos instalar las librerías necesarias para que nuestra aplicación funcione correctamente.

```npm install```

Y haremos uso del siguiente comando para que no nos dé el error sh: 1: nodemon: not found.

```npm install nodemon --save--dev```
![alt text](./imagenes_actividad_3_2/image-3.png)

Y desplegamos nuestra aplicación.
![alt text](./imagenes_actividad_3_2/image-4.png)

Y hacemos la comprobación de que accede correctamente.
![alt text](./imagenes_actividad_3_2/image-5.png)

# Parte dos de la práctica.

Nos conectaremos mediante ssh desde nuestra máquina local a la máquina virtual de la práctica.

![alt text](./imagenes_actividad_3_2/image-6.png)

Y nos generaremos una carpeta para nuestro proyecto y dentro nuestro html y un js con el contenido facilitado en la práctica.

![alt text](./imagenes_actividad_3_2/image-7.png)

![alt text](./imagenes_actividad_3_2/image-8.png)

![alt text](./imagenes_actividad_3_2/image-9.png)

![alt text](./imagenes_actividad_3_2/image-10.png)

Y creamos nuestra aplicacion Node.js con el comando ```npm init``` el cual nos creará nuestro package.json.

![alt text](./imagenes_actividad_3_2/image-11.png)

Y comprobamos que nuestra aplicación funciona correctamente de manera local.

![alt text](./imagenes_actividad_3_2/image-12.png)

![alt text](./imagenes_actividad_3_2/image-13.png)

### Despliegue aplicación en Netlify.

Para comenzar con nuestro despliegue, deberemos de clonar un nuevo repositorio en nuestra máquina. 

Para ello, mediante ssh, haremos la clonación de nuestro repositorio.

![alt text](./imagenes_actividad_3_2/image-14.png)

Accederemos al directorio del repositorio e instalaremos los modulos de netlify necesarios mediante 

```npm install netlify-cli -g```

![alt text](./imagenes_actividad_3_2/image-15.png)

Para poder continuar con la práctica, deberemos de crearnos una cuenta en Netlify y generar un token.

Para generar un token, deberemos de acceder a nuestro perfil y en Aplicaciones nos aparecerá la opción de generar nuevo token.

![alt text](./imagenes_actividad_3_2/image-17.png)

Y seguriemos los pasos:

![alt text](./imagenes_actividad_3_2/image-18.png)

Tras eso, ya tendremos nuestro token y lo que deberemos de hacer una exportacion de nuestro token almacenandolo en una variable. Para ello haremos lo siguiente:

![alt text](./imagenes_actividad_3_2/image-19.png)

Con él, ahora podremos hacer login en Netlify mediante el token y este comando.

![alt text](./imagenes_actividad_3_2/image-20.png)

Tras ello, podremos realizar el despliegue de nuestra aplicación mediante el comando 

```netlify deploy```

Generando uno nuevo.
Añadiendole un Team.
El nombre del sitio.
Y añadiendo como ruta de despliegue el ./build.

![alt text](./imagenes_actividad_3_2/image-21.png)

Tras esto, si cogemos la direccion http que nos muestra el resultado.

![alt text](./imagenes_actividad_3_2/image-23.png)

Despues de comprobar que todo esté correcto, deberemos realizar el despliegue a produccion mediante:

```netlify deploy --prod```

![alt text](./imagenes_actividad_3_2/image-22.png)

Y podremos verlo en nuestro apartado perfil de Netlify.

### Despliegue de aplicación Netlify a través de Github.

Para ello, deberemos de eliminar el despliegue que habíamos creado anteriormente.

![alt text](./imagenes_actividad_3_2/image-24.png)

Y eliminar el repositorio que clonamos anteriormente en nuestra máquina.

![alt text](./imagenes_actividad_3_2/image-25.png)

Tras esto, importaremos un .zip de un repositorio haciendo uso del siguiente comando.

![alt text](./imagenes_actividad_3_2/image-26.png)

Una vez realizado esto, crearemos una carpeta en la que almacenaremos todo el contenido de nuestro proyecto descomprimido. 

Primero, deberemos de realizar un ```mkdir``` para crearnos nuestro directorio donde almacenaremos el contenido.

Tras ello, ```unzip main.zip -d directorio_creado``` para descomprimir el archivo .zip en el directorio creado.

![alt text](./imagenes_actividad_3_2/image-27.png)

Ahora, deberemos de acceder dentro de nuestro repositorio.

![alt text](./imagenes_actividad_3_2/image-28.png)

Y crearnoslo en nuestro repositorio personal de Github.

![alt text](./imagenes_actividad_3_2/image-29.png)

Una vez lo tengamos nos debería de aparecer algo tal que así en nuestro repositorio de github.

![alt text](./imagenes_actividad_3_2/image-30.png)

Ahora, para el despliegue de nuestra aplicación desde un repositorio de github, deberemos de acceder a Netlify y desde el apartado sites, seleccionaremos importar desde git.

![alt text](./imagenes_actividad_3_2/image-31.png)

Nos pedirá que accedamos a nuestro Github y seleccionemos el repositorio que queramos desplegar para instalar Netlify.

![alt text](./imagenes_actividad_3_2/image-32.png)

una vez selecciondado, nos llevará de nuevo a la página de Netlify con nuestro repositorio.

![alt text](./imagenes_actividad_3_2/image-33.png)

Y pondremos la siguiente configuración.

![alt text](./imagenes_actividad_3_2/image-34.png)
![alt text](./imagenes_actividad_3_2/image-35.png)

Le daremos a desplegar y nos aparecerá el despliegue de nuestra aplicación.

![alt text](./imagenes_actividad_3_2/image-36.png)

Una vez el despliegue se haya realizado, aparecerá lo siguiente:

![alt text](./imagenes_actividad_3_2/image-37.png)

Ahora, para comprobar que funciona, editaremos el archivo de texto plano robots.txt que se encuentra dentro de nuestro. Lo editaremos con un contenido personalizado.

![alt text](./imagenes_actividad_3_2/image-38.png)

Y haremos un comit de nuestros cambios a nuestro repositorio para que se hagan los despliegues de la aplicación de manera automática.

![alt text](./imagenes_actividad_3_2/image-39.png)
![alt text](./imagenes_actividad_3_2/image-40.png)

Y lo podremos comprobar en nuestra página personal de Netlify tras realizar el push.

![alt text](./imagenes_actividad_3_2/image-41.png)

Y tras ello, comprobarlo también a nuestro enlace de despliegue, al apartado del archivo robots.txt.

![alt text](./imagenes_actividad_3_2/image-42.png)