# Práctica 2.2 - Autenticación en Nginx

### Creación de usuarios y contraseñas para el acceso web.

Lo que haremos en este paso será crear un archivo oculto .htpasswd en el directorio de configuración donde guardaremos nuestros usuarios y contraseñas para el acceso a la web.
Para ello, usaremos el siguiente comando.

![alt text](./images_actividad_2_2/image.png)

Y después, crearemos una contraseña que cifrará al usuario.

![alt text](./images_actividad_2_2/image-1.png)

### TAREA .- 

Crear dos usuarios, uno con tu nombre y otro con tu primer apellido.

![alt text](./images_actividad_2_2/image-2.png)

Comprueba que el usuario y la contraseña aparecen cifrados en el fichero .htpasswd

![alt text](./images_actividad_2_2/image-3.png)

### Configurando el servidor Nginx para usar autenticación básica.

Debemos de editar nuestro archivo de configuración para añadir la configuración para que nginx utilice el fichero que previamente hemos creado y podamos así usarlo en nuestra página para que pida el acceso de usuario.

![alt text](./images_actividad_2_2/image-4.png)

Y una vez finalicemos, reiniciaremos nuestro servicio nginx.

![alt text](./images_actividad_2_2/image-5.png)

### Probando la nueva configuración.

### TAREA.-

Intentamos iniciar con un usuario.
![alt text](./images_actividad_2_2/image-6.png)


### TAREA.- 

Borra las dos líneas que hacen referencia a la autenticación básica en el location del directorio raíz. Tras ello, añade el nuevo location dentro con la autenticación básica para el archivo/sección contact.html únicamente.

![alt text](./images_actividad_2_2/image-10.png)

Para ello, como no podemos hacer uso de #contact debemos de crearnos un contact.html a parte con el contenido de #contact en nuestro directorio del proyecto para que podamos hacer referencia a él desde el archivo de configuración. 
Una vez lo tengamos creado, con todo el contenido, debemos de añadir la configuración para que nuestro sistema pida la autenticación de usuario cuando se quiera acceder a esa página y no nos dejará acceder nada más que a contact.

![alt text](./images_actividad_2_2/image-9.png)




### Comprobación de autenticación básica con la restricción de acceso por IP.

En este paso, permitiremos y denegaremos el acceso a la ip de nuestra máquina. Para ello debemos de añadir en nuestro archivo de configuración
lo siguiente.

### TAREA.-

Configura Nginx para que no deje acceder con la IP de la máquina anfitriona al directorio raíz de una de tus dos webs. Comprueba que se deniega el acceso:

![alt text](./images_actividad_2_2/image-11.png)

Muestra página de error en el navegador.

![alt text](./images_actividad_2_2/image-12.png)

Muestra el mensaje de error de error.log.

![alt text](./images_actividad_2_2/image-13.png)

### TAREA.- 

Configura Nginx para que desde tu máquina anfitriona se tenga que tener tanto una IP válida como un usuario válido, ambas cosas a la vez, y comprueba que si puede acceder sin problemas.

![alt text](./images_actividad_2_2/image-14.png)

