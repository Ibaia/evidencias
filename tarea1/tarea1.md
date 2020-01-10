+ [Indice](../README.md)
##Instalar en amazon webservice:

* Conectarse al servidor por SSH
![Conectarse al server](Screenshot_1.jpg)

* Hacer update en el servidor, con el comando `Sudo apt-get update`
![Update](Screenshot_2.jpg)

* Instalar apache2 con el comando `sudo apt install apache2 `:
![InstalarApache2](Screenshot_3.jpg)

* Instalar mySql con  `sudo apt-get install mysql-server`:
![InstalarMysql](instalarMySQL.jpg)

* Posterior mente introduces el comando `sudo ysql_secure_installation`
![](SecurityScript1.jpg)

* Aceptas la validacion de contraseña para tener una comporbacion y selecionar una contraseña
![](SecurityScript2.jpg)

* Seleccionas el tipo de contraseña y cual seria
![](SecurityScript3.jpg)

* Seleccionas si quieres borrar los usuarios anonimos y permitir el acceso remoto al mySQL: 
![](SecurityScript4.png)

* Instalar PHP:
Con el comando `sudo apt install php libapache2-mod-php php-mysql` lo instalamos 
![](phpInstalation.jpg)
