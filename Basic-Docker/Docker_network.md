### docker network 
berfungsi untuk membuat jaringan didalam docker 

Jenis network
- Bridge : driver yang digunkan untuk membuat network secara virtual yang memungkinkan containeryang terkoneksi pada jaringan yang sama bisa berkomunikasi
- Host : driver yang membuat network yang sama dengan sistem host, hanya jalan di linux
- None : driver untuk membuat driver tidak bisa berkomunikasi

### list network
```
docker network ls
```

### membuat network
```
docker network create namanetwork
```

jika ingin memilih network driver
```
docker network create --driver namadriver namanetwork
```

### hapus network
```
docker network rm namanetwork
```
NETWORK TIDAK BISA DIHAPUS JIKA MASIH DIGUNAKAN OLEH CONTAINER

### hapus network dari container
```
docker network disconnect namanetwork namacontianer
```

### menambah network ke contianer
```
docker network connect namanetwork namacontianer
```