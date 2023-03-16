# Docker y Linux

```shell
// Generar backup de volumen 
$ docker run --rm --volumes-from <CONTAINER_NAME> -v $(pwd)/backups/webprincipal/desarrollo/uploads:/uploads-backups ubuntu tar cvf /uploads-backups/backup-`date +"%Y-%m-%d"`.tar  /opt/app/public/uploads


// Restore de volumen backup
$ docker run --rm --volumes-from <CONTAINER_NAME> -v $(pwd)/backups/webprincipal/desarrollo/uploads:/uploads-backups ubuntu bash -c "rm -r /opt/app/public/uploads/* && cd /opt/app/public/uploads && tar xvf /uploads-backups/backup-2023-02-18.tar --strip 1"

// Lista archivos dentro de archivo.tar
$ tar -tvf <FILENAME>.tar

// ver el size de un archivo
$ du -h <FILE> 
```
 
 listar archivos dentro de archivo.tar
 
 SELECT * FROM (SELECT * FROM INFOQUERY.VISTA_OS) WHERE ROWNUM <= 100 

