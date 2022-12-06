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
docker run --name devtest -v ${pwd}/html:/usr/local/apache2/htdocs/ -d -p 4300:80 my-apache2

3.e/
docker stop devtest
docker rm devtest

3.f/
docker run --name devtest -d -p 4300:80 my-apache2
docker cp ./html/index.html devtest:/usr/local/apache2/htdocs/

4.a/Voir Dockerfile

4.b/