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
