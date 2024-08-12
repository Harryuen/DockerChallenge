<a name="br1"></a> 

Challenges

Challenge 3 – Full-stack application

Steps

![image](https://github.com/user-attachments/assets/dd88c70b-99a3-4e05-a059-bccb20d9b7d2)

Extract the files present on challenge3.zipto the challenge’s root folder.

•![alt text](image-1.png)

Create a .envfile with the appropriate values (refer to the configuration variables

described below).

Config: These variables

(DB\_ROOT\_PASSWOR

D, DB\_DATABASE,

DB\_USERNAME,

DB\_PASSWORD,

DB\_HOST) define how

the application will

connect to the

database, ensuring the

application knows which

database to use and

with what credentials.

•



<a name="br2"></a> 

•

Create the docker-compose.ymlwith all 3 services:

o nginx

o node-service

o db

![alt text](image-2.png)

built from the ./db directory. It

configures the database

environment with variables like

MYSQL\_ROOT\_PASSWORD and

MYSQL\_DATABASE



<a name="br3"></a> 

![alt text](image-3.png)

It connects to the

database via

environment variables

like DB\_HOST and

DB\_DATABASE, which

are mapped from the

.env file.

It routes incoming

traffic from port 8080 to

the node-service

running on port 3000.

•

Check if all services are running properly.

o Using your browser, access the address <http://localhost:8080/api/books>

If the result is not expected, then return and fix it.

.

o Now open the URL: <http://localhost:8080/api/books/1>

If the result is not expected, then return and fix it.

.

Expected outcomes

•

When you access the following URLs:

o “http://localhost:8080/api/books” you will get a JSON message with all

books.
![alt text](image-4.png)

o “http://localhost:8080/api/books/1” you will get a JSON message with

just one book.

![alt text](image-5.png)

<a name="br4"></a> 

•![alt text](image-6.png)

When executing the command “docker-compose ps”, you should see something

similar to:

