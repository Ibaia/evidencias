+ [Indice](../README.md)
### TAREA 7

* se crea una carpeta en la que guardas los backups:


* Creas el PHP para ejecutar apuntando al .sh:
![](crearElArchivo.jpg)
![](phpPage.jpg)

* Crear el script .sh:
![](shScript.jpg)

* Das permisos a la carpeta del en la que tienes el PHP:
![](darPermisosaServidor.jpg)
![](masPermisos.jpg)

* Dar  permisos a la carpeta en la que tienes el .sh y el cual almacenara las copias de seguridad:
![](darPermisosaBackup.jpg)


* Cambiar usuarios:
![](cambiarUsuario.jpg)

* Comprobar que todo funciona:
![](comprobacionfinal.jpg)


##### Automatizar los backups

* Creamos con crontab para hacer el backup una tarea a ejecutar en nuestro caso `0 20 * * * php /var/www/servidor/script.php`
![](crontab.jpg)

* Creamos con crontab para hacer que los archivos con mas de 7 dias sean borrado, en nuestro caso `20 * * * 6 find /home/backup/server-* -mtime +7 -exec rm {} \;`
![](crontabBorrado.jpg)