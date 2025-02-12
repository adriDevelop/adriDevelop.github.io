# Práctica 6.1.- Dockerización del despliegue de una Aplicación con Node.js

## Despliegue con Docker
Lo primero que deberemos de hacer es instalar Docker en nuestro sistema.
![alt text](./imagenes_actgividad_6_1/image-78.png)

Tras esto, el siguiente paso que deberemos de realizar será el clonar el repositoprio de GitHub [https://github.com/raul-profesor/DAW_practica_6.1_2024.git](https://github.com/raul-profesor/DAW_practica_6.1_2024.git)
![alt text](./imagenes_actgividad_6_1/image-79.png)

Cuando tengamos el repositorio clonado, deberemos modificar el Dockerfile que vendrá con algunos datos en blanco que deberemos de rellenar de la siguiente manera
![alt text](./imagenes_actgividad_6_1/image-80.png)

Una vez editado el archivo, deberemos de construir la imagen librodirecciones
![alt text](./imagenes_actgividad_6_1/image-81.png)
![alt text](./imagenes_actgividad_6_1/image-82.png)

E iniciaremos el contenedor para que escuche peticiones en el puerto 3000 siguiendo este comando
![alt text](./imagenes_actgividad_6_1/image-83.png)

Y al probarlo, nos debería de salir la siguiente pestaña
![alt text](./imagenes_actgividad_6_1/image-84.png)

## Docker Compose
Para poder hacer uso de Docker Compose, deberemos de instalarlo en nuestro sistema.
![alt text](./imagenes_actgividad_6_1/image-85.png)

Comprobaremos la versión que se nos ha instalado de la siguiente manera
![alt text](./imagenes_actgividad_6_1/image-86.png)

Ahora, deberemos de crear un archivo llamado docker-compose.yml en el que deberemos de añadir el siguiente contenido
![alt text](./imagenes_actgividad_6_1/image-87.png)

Una vez creado el archivo, debemos correr la imagen para que se creen todas las tablas que hemos definido en el archivo docker-compose.yml
![alt text](./imagenes_actgividad_6_1/image-88.png)

Una vez ejecutado el comando, deberemos de ejecutar el siguiente comando para que se inicie el contenedor
![alt text](./imagenes_actgividad_6_1/image-89.png)

Y para probar que funciona correctamente, ejecutaremos lo siguiente
![alt text](./imagenes_actgividad_6_1/image-90.png)
![alt text](./imagenes_actgividad_6_1/image-91.png)

# Ejercicios

Añade una persona: ```curl -X PUT http://localhost:3000/persons -H'Content-Type: application/json' -d '{"id": 1, "firstName": "Raúl", "lastName": "Profesor"}```

Listar todas las personas: ```curl -X GET http://localhost:3000/persons/all -H 'Content-Type: application/json'```

Buscar una persona por ID: ```curl -X GET http://localhost:3000/persons/1 -H 'Content-Type: application/json'```

Eliminar una persona: ```curl -X DELETE http://localhost:3000/persons/1 -H 'Content-Type: application/json'```
