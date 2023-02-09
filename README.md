# Docker y Linux

```shell
// Generar backup de volumen 
$ docker run --rm --volumes-from <CONTAINER_NAME> -v $(pwd):/uploads-backups ubuntu tar cvf /uploads-backups/backup-`date +"%Y-%m-%d"`.tar  /opt/app/public/uploads


// Restore de volumen backup
$ docker run --rm --volumes-from dbstore2 -v $(pwd):/backup ubuntu bash -c "cd /dbdata && tar xvf /backup/backup.tar --strip 1"

// Lista archivos dentro de archivo.tar
$ tar -tvf <FILENAME>.tar

// ver el size de un archivo
$ du -h <FILE> 
```
 
 listar archivos dentro de archivo.tar
