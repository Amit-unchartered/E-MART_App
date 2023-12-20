# Containerizing a Microservice E-Commerce Application with Multiple Microservices

## App Description
The app is an ecommerce application with multiple microservices. There are four services in total in the microservice app. To begin, NGINX serves as the API gateway, which is the front end from which all requests are received. This API gateway handles all communications between the other services. It listens for requests and routes them based on the headers in the URL. So, if a request is received on a /, that is, if you are simply accessing the URL, it is routed to the client microservice, which is written in Angular. This loads the website’s frontend pages. The Emart api, written in NodeJS, is contacted for backend data, through the /api. The NodeJs service requires a database, and we use MongoDB, a NoSQL database, in this case. There is also another integration of another service, the Books api, which is written in Java. It makes use of the MySQL database, which is accessed via /webapi. 

**Archietecture Image**
![Image](https://user-images.githubusercontent.com/37503046/215137041-b213faae-fb20-45d0-b3e6-27a1275d804a.png)
