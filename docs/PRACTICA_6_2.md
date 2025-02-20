# Practica 6_2 .- Despliegue de una aplicación PHP con Nginx y MySQL usando Docker y docker-compose

## Lo primero que debemos de hacer es conectarnos mediante ssh a nuestro servidor desde nuestra terminal
![alt text](./imagenes_actividad_6_2/image-78.png)

## 2.- Estructura de directorios
Debemos de configurar la siguiente estructura de directorios 
![alt text](./imagenes_actividad_6_2/image-79.png)

Mediante estos comandos
![alt text](./imagenes_actividad_6_2/image-80.png)

## 3.- Crear archivo docker-compose con configuración de Nginx
Deberemos de crear nuestro archivo docker-compose.yml con la siguiente configuración para instalar la imagen de nginx
![alt text](./imagenes_actividad_6_2/image-81.png)

## 4.- Comprobación de funcionamiento de Nginx
![alt text](./imagenes_actividad_6_2/image-82.png)

![alt text](./imagenes_actividad_6_2/image-84.png)

![alt text](./imagenes_actividad_6_2/image-83.png)

## 5.- Creación del contenedor de PHP
Ahora, deberemos de editar el archivo index.php que se encuentra en www/html/index.php con el siguiente contenido
![alt text](./imagenes_actividad_6_2/image-85.png)

Tras esto, deberemos de configurar el archivo .conf de ./nginx/default.conf con el siguiente contenido
![alt text](./imagenes_actividad_6_2/image-87.png)

Una vez realizada la configuración, deberemos de editar nuestro Dockerfile de la misma direccion ./nginx/Dockerfile con el siguiente contenido
![alt text](./imagenes_actividad_6_2/image-88.png)

Y editaremos la configuración de nuestro docker-compose.yml con la siguiente configuración
![alt text](./imagenes_actividad_6_2/image-89.png)

Levantaremos de nuevo nuestro contenedor mediante el comando ```docker-compose up -d```
![alt text](./imagenes_actividad_6_2/image-91.png)

Y se deberá de ver lo siguiente
![alt text](./imagenes_actividad_6_2/image-90.png)

## 6.- Creación del contenedor para los datos
Deberemos de editar nuestro docker-compose.yml con el siguiente contenido
![alt text](./imagenes_actividad_6_2/image-92.png)

Y deberemos de levantar el contenedor mediante el comando ```docker-compose up -d```
![alt text](./imagenes_actividad_6_2/image-93.png)

## 7.- Creación del contenedor de MySQL
Antes de instalar nuestro contenedor MySQL, deberemos de editar nuestro Dockerfile situado en la ruta ./php/Dockerfile con la siguiente configuración
![alt text](./imagenes_actividad_6_2/image-94.png)

Después, deberemos de actualizar nuestro docker-compose.yml con lo siguiente
![alt text](./imagenes_actividad_6_2/image-96.png)

Y tambien, editaremos nuestro index.php situado en ./www/html/index.php con el siguiente contenido
![alt text](./imagenes_actividad_6_2/image-95.png)

Y deberemos de levantar nuestro contenedor mediante el comando ```docker-compose up -d```

Y se verá lo siguiente
![alt text](./imagenes_actividad_6_2/image-97.png)

## 8.- Comprobación de funcionamiento de la aplicación
Ahora, cambiaremos la configuración de nuestro archivo index.php situado en ./www/html/index.php con el siguiente contenido para que inicie con el usuario root y podamos ver las bases de datos
![alt text](./imagenes_actividad_6_2/image-98.png)

Levanta de nuevo el contenedor mediante el comando ```docker-compose up -d```

Y se deberá de ver lo siguiente
![alt text](./imagenes_actividad_6_2/image-99.png)