# Basic Docker LAMP

> [!PRE-REQUISITES]
> On windows host install wsl and setup ubuntu distro and docker/docker-compose within ubuntu
> On linux host just install docker and docker-compose

> [!PROCEDURE]
> Clone this repo and update your specific php/mysql version in the ```docker-compose.yaml``` file
> execute the command: ```docker-compose up -d```

>you will see the following similar output:
```
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                     NAMES
38ceb9122f8a   phpmyadmin/phpmyadmin   "/docker-entrypoint.…"   22 minutes ago   Up 22 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   lamp_phpmyadmin_1
923ce3aaba79   php:8.2-apache          "docker-php-entrypoi…"   22 minutes ago   Up 19 minutes   0.0.0.0:80->80/tcp, [::]:80->80/tcp       lamp_web_1
c48d790449df   mysql:8.1.0             "docker-entrypoint.s…"   22 minutes ago   Up 22 minutes   3306/tcp, 33060/tcp                       lamp_db_1
```

> Launch your browser and open phpmyadmin ```http://localhost:8080``` to manage mysql data and use the default mysql credential in docker-compose.yaml file meanwhile to access the > php page use ```http://localhost```