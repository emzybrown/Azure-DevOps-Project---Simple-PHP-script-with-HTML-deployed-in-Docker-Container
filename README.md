# Azure-DevOps-Project---Simple-PHP-script-with-HTML-deployed-in-Docker-Container
Azure-DevOps-Project---Simple-PHP-script-with-HTML deployed in Docker Container

1. Code created on a Linux machine as index.php
2. The Dockerfile was created on the same path as the code
3. Docker image was created and run with the below commands exposing app to port 8080
a. docker build -t my-php-app .
b. docker run -p 8080:80 my-php-app
4. Access the PHP script from the browser via http://" Ip address":8080



Push the Docker Images to the Azure container registry and run the image on Azure container instance

1. Create an Azure Container Registry (ACR)
2. Login to ACR: Use the Azure CLI to log in to your ACR:  az acr login --name <YourRegistryName>
3. Tag and Push the Image: Tag your Docker image with the ACR name and push it to the registry:
   a. docker tag my-php-app <YourRegistryName>.azurecr.io/my-php-app:v1
   b. docker push <YourRegistryName>.azurecr.io/my-php-app:v1
4. Create an Azure Container Instance:
a. In the Azure Portal, click "Create a resource" and search for "Container Instances".
b. Provide a resource group, container name, and region.
c. Under the "Container" tab, specify the image from your ACR (e.g., YourRegistryName.azurecr.io/my-php-app:v1).
d. Set the port to 80.
e. Configure other settings such as CPU, memory, and environment variables if necessary.
f. Review and create the container instance.
g. Access the Container: After deployment, you’ll get a public IP address where you can access your PHP script.


OR
Create Azure app service using container image on the Azure container repository
Chuk Ekeh testing
