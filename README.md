Veamos, esto lo he cogido de aquí: https://hackernoon.com/how-to-debug-php-container-with-xdebug-and-phpstorm-1b2k3yjo
Y he hecho un git clone de aquí: https://github.com/ikknd/docker-study

Aparte de eso, hay algún cambio:
* En el docker-compose, el ejemplo parte de una imagen existente "php-xdebug-custom". Yo he hecho que parta de un build y he metido el Dockerfile en una carpeta con ese nombre
* En el docker-compose, obviamente el mapeo de volúmenes cambia (las rutas locales)
* Otra obviedad es que hay que añadir el myapp.loc al /etc/hosts

Para ponerlo en marcha:
* Ir a la carpeta recipe-09/docker y hacer docker-compose up
* Quizá lo más importante: hay que darle al botón de que escuche peticiones php debug en el 9000
* Después únicamente ir a http://myapp.loc/prueba.php y funcionan los breakpoints. Te salta la opcion automatica para que hagas el path mapping

Hasta aquí lo mío

---------------------
---------------------
---------------------
# Docker study project #

* recipe-01 - Nginx docker compose setup - How to run HTML page inside docker - https://hackernoon.com/nginx-docker-how-to-get-html-page-up-with-local-domain-name-b22533nk

* recipe-02 - PHP + Nginx docker compose setup - How to run PHP page inside docker - https://hackernoon.com/nginx-php-docker-how-to-get-php-page-up-with-local-domain-name-ho3x33f6

* recipe-03 - MySQL + phpMyAdmin + PHP docker compose setup - How to run local MySQL database inside docker - https://hackernoon.com/mariadb-phpmyadmin-docker-running-local-database-ok9q36ji

* recipe-04 - Redis + Redis commander docker compose setup - How to run Redis locally inside docker - https://hackernoon.com/how-to-configurate-redis-redis-commander-docker-616136f2

* recipe-05 - PHP Composer usage in docker - https://hackernoon.com/get-composer-to-run-on-docker-container-a-how-to-guide-y86g36z7

* recipe-06 - CRON usage with Docker - https://hackernoon.com/how-to-setup-cron-and-docker-correctly-a-how-to-guide-9v5f36kz

* recipe-07 - Environment variables usage in docker compose - https://hackernoon.com/how-to-use-environment-variables-in-docker-compose-file-l2n32ou

* recipe-08 - How To Extend Docker Compose File - https://hackernoon.com/how-to-extend-docker-compose-file-jc723ypq

* recipe-09 - How to debug PHP container with xdebug and PhpStorm