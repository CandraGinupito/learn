### port forwarding
ini dilakukan jika ingin mengekspos port container
```
docker create --name namacontianer --publish porthost:portcontainer image:tag
```
untuk porthost adalah port yang akan kita akses nanti
sedangkan portcontainer adalah port milik image yang kita gunakan
