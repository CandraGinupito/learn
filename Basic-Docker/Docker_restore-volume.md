### docker volume restore 
digunakan untuk restore data volumem yang telah di backup

```
docker container run --rm --name namecontainer --mount "type=bind,source=/$(pwd)/backup,destination=/backup" --mount "type=volume,source=namevolume,destination=/folder yang mau dibackup" image:tag bash -c "cd /folder yang ingin di restore && tar xvf /backup/backup.tar.gz --strip 1"
```