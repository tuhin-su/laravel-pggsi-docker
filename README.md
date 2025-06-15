[DOCKER IMAGE](https://github.com/tuhin-su/docker.git)

## REQUIRE IMAGES

1. PHP-COMPOSER (php)
2. pgAdmin
3. postgres

## BUILD IMAGE COMMAND (IF NOT EXISTS)

```bash
    git clone https://github.com/tuhin-su/docker.git
    cd docker
    docker build --build-arg VERSION=latest  --build-arg HOST_UID=1000 -f pgadmin.Dockerfile -t pgadmin:local .
    docker build --build-arg VERSION=latest  --build-arg HOST_UID=1000 -f postgress.Dockerfile -t postgress:local .
    docker build --build-arg VERSION=8.2-fpm  --build-arg HOST_UID=1000 -f php.Dockerfile -t php:local-8.2-fpm .
    rm -rf docker
```
#DOMAIN S
```bash
app.ees.test -> main app
db.ees.test -> databse
pgadmin.ees.test -> pgAdmin
```