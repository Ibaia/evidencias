+ [Indice](../README.md)
### FTP

* Se instala con el comando `sudo apt-get install vsftpd`:
![](instalar.jpg)

* Se inicia el servicio y lo activas:
![](iniciar.jpg)
![](iniciar2.jpg)

* creas una copia del archivo de configuacion :
![](CopiaParaModificar.jpg)

* Accedes al archivo original con el comando`sudo nano /etc/vsftpd.conf` y añades las siguientes filas y guardas:
![](vsftpd.conf.jpg)

* Añadir el protocolo ftp al servidor:
![](puertoFTP.jpg)

* Crear usuario con `sudo  useradd -g ftp -d /var/www/carpeta deseada/ -c "Tipo usuario" usuario` y compurebas que exista:
![](crearElUsuario.jpg)
![](verificarElusuario.jpg)

* Reinicias:
![](restart.jpg)