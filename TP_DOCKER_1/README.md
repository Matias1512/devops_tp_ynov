Exercice Docker
3.a/
docker pull httpd

//Build
docker build -t my-apache2 .
docker run -dit --name my-running-app -p 8080:80 my-apache2

http://localhost:8080  "It's Work"

3.b/
docker images
