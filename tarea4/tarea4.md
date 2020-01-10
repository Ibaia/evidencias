+ [Indice](../README.md)
### Virtual host

* Copia el 000-default.conf con el mnombre que desees que el comando `sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/servidor.conf`
![](CopiarElbase.jpg)

* modificas el archivo que acabas de crear con la configuración deseada
![](modificar.jpg)

* Virtual host servidor: 
![](VirtualHost.jpg)

* Añadirlo al apache con el comando `sudo a2ensite cliente.conf`
![](meterloComoEnable.jpg)

* Reiniciar el servidor tras modificar el virtualHost:
![](ReiniciarApache.jpg)

* Vista cliente:
![](cliente.jpg)

* Vista servidor:
![](Servidor.jpg)