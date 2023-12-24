# Containerizing a Microservice E-Commerce Application with Multiple Microservices Locally

## App Description
The e-commerce application is divided into four distinct services:

1. Nginx (API Gateway): This service acts as the central hub for processing incoming requests. It listens to various endpoints (“/”, “/api”, “/webapi”) and routes them accordingly.
2. Angular Client: Responsible for rendering the front end of the website or user interface, accessible through the “/” endpoint.
3. Node.js Backend (Emart API): Manages and takes charge of the business logic and interacts with a MongoDB database. Accessed through the “/api” endpoint.
4. Java Backend (Books API): Another backend service handling book-related functionalities, backed by a MySQL database. Accessed through the “/webapi” endpoint. 

**Archietecture Image**
![Image](https://user-images.githubusercontent.com/37503046/215137041-b213faae-fb20-45d0-b3e6-27a1275d804a.png)

<ins>**The Need for Containerization**</ins>

Containerization provides a standardized and portable environment for applications. It encapsulates each microservice along with its dependencies, ensuring consistency across different environments. Docker, a leading containerization platform, is the tool of choice for this project.

### Initial Steps
1. Clone the repository.
```
$ git clone https://github.com/Amit-unchartered/E-MART_App.git
```
2. Change directory to E-MART_App, then to vagrant
```
$ cd E-MART_App/vagrant
```
3. Do vagrant up, it contains all the commands for docker installation and its dependencies.
```
$ vagrant up
$ vagrant ssh
```
4. Switch to root user
```
$ sudo -i
```

### Project Setup
1. Clone the repository inside the VM.
```
# git clone https://github.com/Amit-unchartered/E-MART_App.git
```
2. change directory into E-MART_App.
```
# cd E-MART_App
```
3. Make sure there are no other containers present, **if present then** to stop and remove the container
```
# docker compose down
```
4. Remove all the earlier containers and images before setting up this project.
```
# docker system prune -a
```
5. Now, we will be orchestrating with docker compose.
```
# docker compose up -d
```
6. The project is set up, if you want to access it from outside the VM, then we must know the VM's IP address
```
# ip addr show
```
***Find for the class C ip address i.e 192.168.x.y, type this ip at top of your browser, it will route the request to port 80.***
