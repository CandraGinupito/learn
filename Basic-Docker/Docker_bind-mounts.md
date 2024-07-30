### bind mounts 
digunakan untuk mounting(shairng) file/folder dari sistem host ke container

tipe mount ada 2 
-bind
-volume

```
docker container --name namacontainer --mount "type=bind,source=folder,destination=folder" image:tag
```

jika hanya ingin readonly 
```
docker container --name namacontainer --mount "type=bind,source=folder,destination=folder,readonly" image:tag
```

