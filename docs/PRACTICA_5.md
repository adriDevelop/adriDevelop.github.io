# Práctica 5  .- Ejercicios Github

## Primera parte .- Repositorio DEAW
Lo primero que debemos de hacer es crear el repositorio DEAW si aún no lo tenemos creado:
![alt text](./imagenes_actividad_5/image-2.png)

Seguimos clonandolo en nuestro repositorio local de la siguiente manera:
![alt text](./imagenes_actividad_5/image.png)

## Segunda parte .- README
Ahora, debemos de generar el README para nuestro repositorio. Para ello haremos lo siguiente:
![alt text](./imagenes_actividad_5/image-1.png)

Seguiremos, haciendo un ```git add README.md``` para que podamos hacerle el commit al archivo y despues realizar el push del mismo.
![alt text](./imagenes_actividad_5/image-3.png)

## Tercera parte .- Commit al archivo README.md
Y hacemos un commit del archivo.
![alt text](./imagenes_actividad_5/image-4.png)

## Cuarta parte .- Push del archivo README.md
Y finalmente el push.
![alt text](./imagenes_actividad_5/image-5.png)

## Quinta parte .- Ignoración de archivos mediante el archivo ".gitignore"
Lo primero que debemos hacer en este paso es generar un fichero ```privado.txt```

Tras la creación de este archivo, generaremos el directorio ```/privada```
![alt text](./imagenes_actividad_5/image-6.png)

Y para que no los tenga en cuenta git, debemos de generar un archivo .gitignore para que ignore tanto el archivo ```privado.txt``` y el directorio ```/privada```
![alt text](./imagenes_actividad_5/image-7.png)

## Sexta parte .- Crear el fichero 1.txt y agregarlo al repositorio local
Se creará y agregará de la siguente manera:
![alt text](./imagenes_actividad_5/image-8.png)

## Séptima parte .- Crear el tag v0.1
Lo creamos usando el comando ```git tag```
![alt text](./imagenes_actividad_5/image-9.png)

## Octava parte .- Subir el tag v0.1
![alt text](./imagenes_actividad_5/image-10.png)

## Novena parte .- Cuenta de github
Deberemos de agregarle a la cuenta de github una foto (si no la tenemos agregada ya)
![alt text](./imagenes_actividad_5/image-12.png)

También, activar la protección doble factor en la cuenta de github, para ello:

1.- Deberemos de irnos a la configuración de nuestro perfil y encontrar " Two-factor authentication"
![alt text](./imagenes_actividad_5/image-11.png)

2.- Tras eso, deberemos de seguir los pasos que nos diga la web. El primero es descargarnos la app móvil y darle permiso desde el teléfono.
![alt text](./imagenes_actividad_5/image-13.png)

3.- El siguiente paso sería escanear un QR en el que agregaremos a nuestro teléfono el ```Two-factor authentication``` y nos dará un código cada vez que queramos acceder a nuestra cuenta. (no pongo captura por seguridad)

4.- El siguiente paso, nos mostrará una serie de códigos de recuperacion que deberemos de guardar en un lugar seguro. Descargaremos y proseguimos.

5.- Ya estaríai activado la protección doble factor en nuestra cuenta de github.
![alt text](./imagenes_actividad_5/image-14.png)

## Décima parte .- Uso social de Github
Deberemos de seguir a dos compañeros de clase en su cuenta de github
![alt text](./imagenes_actividad_5/image-15.png)

Cuando lo tengamos, deberemos de seguir los repositorios de nuestros compañeros y hacerle un star
![alt text](./imagenes_actividad_5/image-16.png)

## Undécima parte .- Crear una tabla mencionando a nuestros compañeros
Para ello, en nuestro README.md, crearemos una tabla en la que mostraremos el nombre y un enlace para poder ir a su repositorio.
![alt text](./imagenes_actividad_5/image-17.png)

## Duodécima parte .- Creación de una rama
A continuación, deberemos de crearnos una rama con nombre v0.2 y posicionarnos en ella.
![alt text](./imagenes_actividad_5/image-18.png)

## Decimotercera parte .- Añadir un fichero a la rama v0.2
Ahora, deberemos de crear un fichero ```2.txt``` y lo añadiremos a la rama v0.2
![alt text](./imagenes_actividad_5/image-19.png)

## Decimocuarta parte .- Merge directo
Ahora, deberemos de posicionarnos en la rama master y realizaremos un merge de la rama v0.2 en la rama master, para ello vamos a usar los siguientes comandos:

1.- Para posicionarnos en la master (que lo tengo nombrado main)
![alt text](./imagenes_actividad_5/image-20.png)

2.- Para hacer el merge de la rama v0.2 en la rama master
![alt text](./imagenes_actividad_5/image-21.png)

## Decimoquinta parte .- Merge con conflicto
Seguiremos ahora generando un conflicto entre las ramas.

Para ello, deberemos de hacer lo siguiente:

1.- En la rama master, editaremos el fichero ```1.txt``` y haremos un commit.
![alt text](./imagenes_actividad_5/image-22.png)

![alt text](./imagenes_actividad_5/image-23.png)

2.- En la rama v0.2 editaremos el fichero ```1.txt``` y haremos el commit.
![alt text](./imagenes_actividad_5/image-24.png)

![alt text](./imagenes_actividad_5/image-25.png)

![alt text](./imagenes_actividad_5/image-26.png)

3.- Ahora, nos posicionaremos en la rama master y haremos un merge con la rama v0.2.
![alt text](./imagenes_actividad_5/image-27.png)

![alt text](./imagenes_actividad_5/image-28.png)

## Decimosexta parte .- Listado de ramas
Ahora, listaremos las ramas con merge y sin merge. Para ello, usaremos lo siguiente:
![alt text](./imagenes_actividad_5/image-29.png)

## Decimoséptima parte .- Arreglar conflicto
Ahora, para arreglar el conflicto, deberemos de editar el archivo de texto ```1.txt``` y una vez editado, haremos un commit y un push.
![alt text](./imagenes_actividad_5/image-30.png)

![alt text](./imagenes_actividad_5/image-31.png)

![alt text](./imagenes_actividad_5/image-32.png)

## Decimoctava parte .- Borrar rama
Seguido de esto, procederemos a borrar la rama v0.2
![alt text](./imagenes_actividad_5/image-33.png)

## Decimonovena parte .- Listado de cambios
Y para finalizar, realizaremos un listado de los distintos commits con sus ramas y sus tags
![alt text](./imagenes_actividad_5/image-34.png)







