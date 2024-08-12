<a name="br1"></a> 

Challenges

Challenge 3 – Full-stack application

Steps

Extract the files present on challenge3.zipto the challenge’s root folder.
![image](https://github.com/user-attachments/assets/dd88c70b-99a3-4e05-a059-bccb20d9b7d2)


Create a .envfile with the appropriate values (refer to the configuration variables

described below).

![image](https://github.com/user-attachments/assets/e88deeed-fc1d-4730-b4dd-cf10f01b90f3)

Config: These variables

(DB\_ROOT\_PASSWORD, DB\_DATABASE,DB\_USERNAME,DB\_PASSWORD,DB\_HOST) define how the application will

connect to the database, ensuring the application knows which database to use and with what credentials.

•


<a name="br2"></a> 

•

Create the docker-compose.ymlwith all 3 services:

o nginx

o node-service

o db

![image](https://github.com/user-attachments/assets/7b7b63af-851b-477c-8d89-2526c65afb91)


built from the ./db directory. It configures the database environment with variables like

MYSQL\_ROOT\_PASSWORD and MYSQL\_DATABASE.



<a name="br3"></a> 

![image](https://github.com/user-attachments/assets/cf05bd39-0fc2-431f-a265-939359b5dfff)

(node-service)It connects to the database via environment variables like DB\_HOST and DB\_DATABASE, which

are mapped from the .env file.

(nginx)It routes incoming traffic from port 8080 to the node-service running on port 3000.

•
Expected outcomes

Check if all services are running properly.

o Using your browser, access the address <http://localhost:8080/api/books>

If the result is not expected, then return and fix it.

.![image](https://github.com/user-attachments/assets/9272ac9e-04da-4c8a-9b8c-459699281a6f)


o Now open the URL: <http://localhost:8080/api/books/1>

If the result is not expected, then return and fix it.

.![image](https://github.com/user-attachments/assets/c5c5db3c-aec1-4a08-8662-f142387fa365)





When executing the command “docker-compose ps”, you should see something

![image](https://github.com/user-attachments/assets/836e8c87-b94c-4f50-b5d5-89a979041d69)

