# Azure-DevOps-Project---Simple-PHP-script-with-HTML-deployed-in-Docker-Container
Azure-DevOps-Project---Simple-PHP-script-with-HTML deployed in Docker Container

1. Code created on a Linux machine as index.php
2. The Dockerfile was created on the same path as the code
3. Docker image was created and run with the below commands exposing app to port 8080
a. docker build -t my-php-app .
b. docker run -p 8080:80 my-php-app
4. Access the PHP script from the browser via http://" Ip address":8080

