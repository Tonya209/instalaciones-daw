# INSTALACION DRUPAL

### 1. Antes de instalar Drupal he instalado MariaDB:
>`sudo apt install mariadb-server`

 Luego he ejecutado el comando
>`sudo apt install apache2 libapache2-mod-php php php-mysql`

para instalar Apache 2 y el módulo que permite Apache 2 intrpretar PHP.

Para comprobar, he creado un fichero `info.php` en la ruta `/var/www/html`

Y vemos la información de PHP: PHP7.4.3.

### 2. Segiendo el video tutorial he instalado Wordpress
### 3. Instalamos Drupal:

- Descargamos Drupal de la página web: 
`https://www.drupal.org/download`

usamos comando:
>`sudo wget https://www.drupal.org/download-latest/tar.gz`

en la carpeta /var/www/html

- descomprimimos con el comando:
>`sudo tar xzf tar.gz`

- creamos directorio `sites/default/files`
>`sudo mkdir sites/default/files`\
>`sudo cp sites/default/default.settings.php sittes/default/settings.php`

- cambiamos los permisos:
>`sudo chmod a+w sites/default/settings.php`\
>`sudo chmod a+w sites/default/files`,\
>`sudo chown www-data:root sites/default/files`

- accedemos a la pagina Dupal y elegimos la idioma
 
- ponemos nombre de la base de datos (wordpress)/usuario (user)/ contraseña (password).

- verificacón de requisitos para la instalación. 
He tenido error: **PHP EXTENSIONS** *Disabled - Drupal requires you to enable the PHP extensions in the following list..*
He usado el comando para resolverlo:
>`sudo apt install php-dom php-gd php-xml php-mysql`\
>`sudo service apache2 restart`

- los últimos pasos: configurar sitio (dar nombre - **Web Ubuntu**/ poner correo electrónico) y terminar traducciones.


