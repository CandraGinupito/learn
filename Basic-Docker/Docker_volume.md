### docker volume
penyimpanan yang di simpan dan di manage oleh docker itu sendiri

*list volume*

```
docker volume ls
```

*create volume*

```
docker vloume create namevolume
```

*hapus volume*

```
docker volume rm namevolume
```
JIKA INGIN MENGHAPUS VOLUME PASTIKAN VOLUME TIDAK DIGUNAKAN OLEH CONTAINER MANAPUN

### menggunakan docker volume
```
docker container --name namecontainer --mount "type=volume,source=namevolume,destination=folder" image:tag
```

### backup volume
jika ingin backup pastikan container yang memakai volume yang ingin dibackup dimatikan, agar container tidak menulis di volume saat backup sedang dijalankan

buat container dulu dengan mount bind dan volume 
```
docker container create --name namecontainer --mount "type=bind,source=/pwd/backup,destination=/backup" --mount "type=volume,source=namevolume,destination=/folder yang mau dibackup" image:tag
```
kemudian masuk ke terminal container
```
docker container exec -i -t namecontainer /bin/bash
```
tar cvf /backup/name.tar.gz /folder yang ingin di backup
```

*stop dan remove container yang baru saja dibuat untuk backup*

### backup dengan docker run

harus dilakukan dengan image yang bisa sekali jalan

```
docker container run --rm --name namecontainer --mount "type=bind,source=/$(pwd)/backup,destination=/backup" --mount "type=volume,source=namevolume,destination=/folder yang mau dibackup" image:tag tar cvf /backup/name.tar.gz /folder yg ingin dibackup
```

 

