Exercice Docker
3.a/
docker pull httpd

//Build
docker build -t my-apache2 .
docker run -dit --name my-running-app -p 8080:80 my-apache2

http://localhost:8080  "It's Work"

3.b/
docker images

3.d/
docker run --name devtest -v ${pwd}/html:/usr/local/apache2/htdocs/ -d -p 4300:80 httpd

3.e/
docker stop devtest
docker rm devtest

3.f/
docker run --name devtest -d -p 4300:80 httpd
docker cp ./html/index.html devtest:/usr/local/apache2/htdocs/

4.a/Voir Dockerfile

4.b/docker build -t my-apache2 .
    docker run -dit --name my-running-app -p 8080:80 my-apache2

4.c/La différence est que avec le Dockerfile on peut directement définir le fichier qui va être ouvert avec l'image

5.a/docker pull mysql
    docker pull phpmyadmin

5.b/docker run --name phpmyadmin -d --link mysql_db_server:db -p 8080:80 phpmyadmin
(marche pas)

6.a/Compose utilise un fichier YAML pour configurer les services de l'application et en une seule commande il crée et démarre tous les services à partir des configurations présent dans le fichier YAML

6.b/docker compose start -nomDuService
    docker compose kill

