### List all container
```
docker container ls -a

docker ps
```

### Membuat container
```
docker create --name namacontianer image:tag
```

### Create docker tanpa harus pull image 
```
docker run -d -t --name namacontainer image:tag
```

### Start container docker
```
docker container start namacontainer/containerid
```

### Stop container docker
```
docker stop namacontainer/containerid
```

### Hapus container docker
```
docker container rm namacontainer/containerid
```