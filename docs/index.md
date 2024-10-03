# Adrián Velasco Carrasco

## Práctica 2.1 - Instalación y configuración de un servidor web Nginx

### Instalación

Para instalar el servidor de nginx en nuestra Debian debemos de realizar los siguientes comandos: <br>
`sudo apt update`
`sudo apt install nginx`

Y comprobamos que se ha instalado y que está funcionando correcamente: <br>
`systemctl status nginx`

### Creación de las carpetas del sitio web

Vamos a crear nuestra carpeta para nuestro sitio web dentro de /var/www ya que típicamente, estas carpetas almacenan los sitios.
Para crearla haremos uso del comando: `sudo mkdir -p /var/www/nombre_web/html`

Y dentro de esta carpeta, debemos clonar el repositorio: `https://github.com/cloudacademy/static-website-example`

Además, haremos que el propietario de esta carpeta y todo lo que haya
