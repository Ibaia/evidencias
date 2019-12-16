##Instalar en amazon webservice:

* Conectarse al servidor por SSH
![Conectarse al server](tarea1/Screenshot_1.jpg)

* Hacer update en el servidor, con el comando `Sudo apt-get update`
![Update](tarea1/Screenshot_2.jpg)

* Instalar apache2 con el comando `sudo apt install apache2 `:
![InstalarApache2](tarea1/Screenshot_3.jpg)

* Instalar mySql con  `sudo apt-get install mysql-server`:
![InstalarMysql](tarea1/instalarMySQL.jpg)

* Posterior mente introduces el comando `sudo ysql_secure_installation`
![](tarea1/SecurityScript1.jpg)

* Aceptas la validacion de contraseña para tener una comporbacion y selecionar una contraseña
![](tarea1/SecurityScript2.jpg)

* Seleccionas el tipo de contraseña y cual seria
![](tarea1/SecurityScript3.jpg)

* Seleccionas si quieres borrar los usuarios anonimos y permitir el acceso remoto al mySQL: 
![](tarea1/SecurityScript4.png)

* Instalar PHP:
Con el comando `sudo apt install php libapache2-mod-php php-mysql` lo instalamos 
![](tarea1/phpInstalation.jpg)

## Establecer una IP elastica
* Buscas la seccion de `Elastic IPs`
![](tarea2/primerClick.jpg)

* Crear la ip elastica:
![](tarea2/CrearIpElastica.jpg)

* Asociar la ip elastica creada:
Clicando en actions:
![](tarea2/action.jpg)

![](tarea2/AsociarIP.jpg)

* Comprobar que funcione: 
![](tarea2/asociada.jpg)

## Crear un registro de DNS

### Tipos de registros:

* A: Dirección (address). Este registro se usa para traducir nombres de servidores de alojamiento a direcciones IPv4.

* AAAA: Este registro se usa en IPv6 para traducir nombres de hosts a direcciones IPv6.

* CNAME: Se usa para crear nombres de servidores de alojamiento adicionales, o alias, para los servidores de alojamiento de un dominio. Es usado cuando se están corriendo múltiples servicios (como FTP y servidor web) en un servidor con una sola dirección IP.

* TXT: Los registros TXT son un tipo de registros de sistema de nombres de dominio (DNS) que contienen información de texto de fuentes externas a tu dominio y que puedes añadir a su configuración.

* SRV:  Service record

### Vincular subdominio con la instacia de AWS

* Accedes al panel del subdominio y entras en registro de DNS.
![](tarea3/registroDNS.jpg)

* Al acceder registros encontraras un formulario
![](tarea3/DatosARellenar.jpg)

* Rellenar los datos y crear el subdominio apuntando a la IpElastica.
![](tarea3/CrearElRegistro.jpg)

### Virtual host

* Copia el 000-default.conf con el mnombre que desees que el comando `sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/servidor.conf`
![](tarea4/CopiarElbase.jpg)

* modificas el archivo que acabas de crear con la configuración deseada
![](tarea4/modificar.jpg)

* Virtual host servidor: 
![](tarea4/VirtualHost.jpg)

* Añadirlo al apache con el comando `sudo a2ensite cliente.conf`
![](tarea4/meterloComoEnable.jpg)

* Reiniciar el servidor tras modificar el virtualHost:
![](tarea4/ReiniciarApache.jpg)

* Vista cliente:
![](tarea4/cliente.jpg)

* Vista servidor:
![](tarea4/Servidor.jpg)