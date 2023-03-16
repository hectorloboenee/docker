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
 
SELECT * FROM (SELECT CLAVE, NOMBRE_CLIENTE, NUM_CONTADOR, DIRECCION, COD_MUNIC, NOM_MUNIC, EST_SUM, DESC_EST, F_ACTUAL, NUM_OS, MULTIPLICADOR, TIP_OS, TIPO_OS, COMENT_OS,  CASE COORD_X WHEN ' ' THEN 'NULL' ELSE COORD_X END AS COORD_X, CASE COORD_Y WHEN ' ' THEN 'NULL' ELSE COORD_Y END AS COORD_Y, LECT_ANT, LECT_ACT FROM INFOQUERY.VISTA_OS) WHERE ROWNUM < 100

