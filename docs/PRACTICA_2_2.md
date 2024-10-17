# Práctica 2.2 - Autenticación en Nginx

### Creación de usuarios y contraseñas para el acceso web.

Lo que haremos en este paso será crear un archivo oculto .htpasswd en el directorio de configuración.
Para ello, usaremos el siguiente comando.

Y después, crearemos un cifrado para el usuario.

### TAREA .- 

Crear dos usuarios, uno con tu nombre y otro con tu primer apellido.

Comprueba que el usuario y la contraseña aparecen cifrados en el fichero .htpasswd

### Configurando el servidor Nginx para usar autenticación básica.

Debemos de editar nuestro archivo de configuración para añadir la configuracion para que nginx utilice el fichero que previamente hemos creado.

Y una vez finalicemos, reiniciaremos nuestro servicio.

### Probando la nueva configuración.

### TAREA.-

Intentamos iniciar con un usuario erroneo y luego con uno correcto. 

Adjuntar captura de pantalla de los logs.


### TAREA.- 

Borra las dos lñineas que hacen referencia a la autenticación básica en el location del directorio raíz. Tras ello, añade el nuevo location dentro con la autenticación básica para el archivo/sección contact.html únicamente.

### Comprobación de autenticación básica con la restricción de acceso por IP.

En este paso, permitiremos y denegaremos el acceso a la ip de nuestra máquina. Para ello debemos de añadir en nuestro archivo de configuración
lo siguiente.

### TAREA.-

Configura Nginx para que no deje acceder con la IP de la máquina anfitriona al directorio raíz de una de tus dos webs. Comprueba que se deniega el acceso:

Muestra página de error en el navegador.

Muestra el mensaje de error de error.log.

### TAREA.- 

Configura Nginx para que desde tu máquina anfitriona se tenga que tener tanto una IP válida como un usuario válido, ambas cosas a la vez, y comprueba que si puede acceder sin problemas.


### Respuesta a las cuestiones.