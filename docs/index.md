# Práctica 2.1 - Instalación y configuración de un servidor web Nginx

### Instalación

Para instalar el servidor de nginx en nuestra Debian debemos de realizar los siguientes comandos: <br>
`sudo apt update`
`sudo apt install nginx`

![alt text](<./images/Captura de pantalla 2024-10-08 a las 23.39.11.png>)

Y comprobamos que se ha instalado y que está funcionando correcamente: <br>
`systemctl status nginx`

![alt text](./images/image.png)

### Creación de las carpetas del sitio web

Vamos a crear nuestra carpeta para nuestro sitio web dentro de /var/www ya que típicamente, estas carpetas almacenan los sitios.
Para crearla haremos uso del comando: `sudo mkdir -p /var/www/adridevelop/html`

![alt text](./images/image2.png)

Para el siguiente paso, deberemos de instalar git en Debian. Para ello realizamos lo siguiente.
![alt text](./images/image3.png)

Y dentro de esta carpeta, debemos clonar el repositorio: `https://github.com/cloudacademy/static-website-example`

![alt text](./images/image4.png)

Ahora, haremos que el usuario www-data sea el propietario mediante el comando `sudo chown -R www-data:www-data /var/www/adridevelop/html`.

![alt text](./images/image5.png)

A continuación, daremos los permisos necesarios para no tener errores en el acceso al sitio web usando el comando `sudo chmod -R 755 /var/www/adridevelop`

![alt text](./images/image-1.png)

Y comprobaremos que está funcionando desde nuestra máquina local escribiendo en la barra de búsqueda la ip de nuestro servidor.

![alt text](./images/image6.png)

### Configuración de servidor web NGINX

Para que podamos presentar contenido en nuestra webm deberemos de crear un bloque de servidor con directivas correctas. Para ello, crearemos un nuevo archivo de configuración. Iremos a nuestra terminal y crearemos nuestro archivo de configuración mediante `sudo nano /etc/nginx/sites-available/vuestro_dominio`.

![alt text](./images/image7.png)

Y dentro de este archivo que hemos creado, generaremos lo siguiente:

```
server {
        listen 80;
        listen [::]:80;
        root /ruta/absoluta/archivo/index;
        index index.html index.htm index.nginx-debian.html;
        server_name nombre_web;
        location / {
                try_files $uri $uri/ =404;
        }
}
```

![alt text](./images/image8.png)

También, deberemos de crear un archivo simbólico entre este archivo y el de los sitios que están habilitados. Para ello `sudo ln -s /etc/nginx/sites-available/nombre_web /etc/nginx/sites-enabled/`

![alt text](./images/image9.png)

Y reiniciaremos el servidor. `sudo systemctl restart nginx`

![alt text](./images/image10.png)

### Comprobaciones

Para comprobar que nuestro host está funcionando, deberemos de acceder dentro de nuestra máquina cliente a /etc/host y añadiremos nuestro servidor nginx.

![alt text](./images/image11.png)

Y deberemos también comprobar que, las peticiones se están registrando correctamente en los archivos de logs, tanto las correctas como las erróneas.

![alt text](./images/image12.png)

![alt text](./images/image13.png)

![alt text](./images/image14.png)

![alt text](./images/image15.png)

### FTP

Para configurar SFTP en Debian deberemos de instalar antes vsftpd, para ello, haremos uso de `sudo apt-get install vsftpd`

![alt text](./images/image16.png)

Tras eso, crearemos una carpeta en nuestro home de Debian llamada ftp. `mkdir /home/adrian-alumno/ftp`

![alt text](./images/image17.png)

Tras eso, deberemos de crear los certificados de seguridad necesarios mediante `sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/vsftpd.pem -out /etc/ssl/private/vsftpd.pem`

![alt text](./images/image18.png)

Y una vez realizados estos pasos, deberemos de editar el documento /etc/vsftpd.conf de la siguiente manera: `sudo nano /etc/vsftpd.conf`

![alt text](./images/image19.png)

Y guardaremos los cambios y reiniciaremos el servidor. `sudo systemctl restart -now vsftpd`

![alt text](./images/image20.png)

Tras esta configuración, instalaremos FileZilla y haremos una operación ftp a nuestro servidor. Para ello, deberemos de poner nuestra ip, nombre de usuario, contraseña y puerto para que podamos realizar la conexión. 

![alt text](./images/image21.png)

Tras haber realizado la conexión correctamente, debemos pasar un archivo para comprobar que funciona, en mi caso, una foto.

![alt text](./images/image22.png)

![alt text](./images/image23.png)

### HTTPS 

Deberemos de instalar openssl para que podamos acceder a nuestro sitio a través de https.

![alt text](./images/image24.png)

Ahora, crearemos nuestro certificado.

![alt text](./images/image25.png)

Y tras eso, almacenaremos la configuración.

![alt text](./images/image26.png)

Y agregaremos el cerficado y las nuevas rutas a nuestro fichero.

![alt text](./images/image27.png)

Y en nuestro host, añadiremos en nuestra ip, las direcciones añadidas anteriormente.

![alt text](./images/image28.png)

Y buscamos en nuestro navegador nuestro sitio web.

![alt text](./images/image29.png)

![alt text](./images/image30.png)
