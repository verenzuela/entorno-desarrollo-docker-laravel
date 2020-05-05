# entorno-desarrollo-docker-laravel


### Clonar

- Clonar este repositorio usando ` git clone https://github.com/verenzuela/entorno-desarrollo-docker-laravel.git`

- El contenedor de BD tiene por defecto: usuario:root clave:secret

### Uso

- Para usar este proyecto debe tener instalado Docker y docker-compose.
- Crear un virtual host en su equipo: laravel-desdecero.io, si lo crea con otro nombre debe reemplazar en los archivos vhost.conf y docker-compose.yaml
- Crear un proyecto laravel dentro de www llamado curso, su usted crea el proyecto con un nombre diferente debe reemplazar el nombre de la carpteta en los archivos vhost.conf y docker-compose.yaml

> Ejecutar contenedor
- en el terminal navege hasta la carpeta de entorno-desarrollo-docker-laravel y ejecute

```shell
$ docker-compose up
```

> Si desea ejecutar el contenedor en background ejecute

```shell
$ docker-compose up -d
```


> Para detener los contenedores, ejecute

```shell
$ docker-compose down
```