\# Flask CRUD REST API



A simple CRUD (Create, Read, Update, Delete) REST API built using \*\*Python Flask, Flask-SQLAlchemy, PostgreSQL, and Docker\*\*.



This project demonstrates how to develop a backend REST API, connect it to a PostgreSQL database, containerize the application using Docker, and test the API using Postman.



\---



\## 🚀 Project Overview



The Flask CRUD REST API allows users to perform basic database operations through REST API endpoints.



The application uses:



\* \*\*Flask\*\* for the backend REST API

\* \*\*Flask-SQLAlchemy\*\* for database operations

\* \*\*PostgreSQL\*\* as the relational database

\* \*\*Docker\*\* for containerization

\* \*\*Docker Compose\*\* for managing Flask and PostgreSQL

\* \*\*Postman\*\* for API testing

\* \*\*Git \& GitHub\*\* for version control



\---



\## 🛠️ Technologies Used



| Technology       | Purpose                      |

| ---------------- | ---------------------------- |

| Python           | Programming Language         |

| Flask            | Backend Web Framework        |

| Flask-SQLAlchemy | ORM / Database Integration   |

| PostgreSQL       | Relational Database          |

| Docker           | Application Containerization |

| Docker Compose   | Multi-container Management   |

| Postman          | API Testing                  |

| Git              | Version Control              |

| GitHub           | Code Repository              |



\---



\## ✨ Features



\* Create a new user

\* Retrieve all users

\* Retrieve a user by ID

\* Update an existing user

\* Delete a user

\* PostgreSQL database integration

\* SQLAlchemy ORM

\* Docker containerization

\* Docker Compose configuration

\* REST API testing using Postman



\---



\## 📁 Project Structure



```text

flask-crud-api/

│

├── app.py

├── Dockerfile

├── docker-compose.yml

├── requirements.txt

├── README.md

└── .gitignore

```



\---



\## 🔄 CRUD Operations



| Operation | HTTP Method | Endpoint      | Description             |

| --------- | ----------- | ------------- | ----------------------- |

| Create    | POST        | `/users`      | Create a new user       |

| Read All  | GET         | `/users`      | Retrieve all users      |

| Read One  | GET         | `/users/<id>` | Retrieve a user by ID   |

| Update    | PUT         | `/users/<id>` | Update an existing user |

| Delete    | DELETE      | `/users/<id>` | Delete a user           |



\---



\# 🌐 API Endpoints \& Outputs



\## 1. Check API Status



\### Request



\*\*GET\*\*



```text

http://127.0.0.1:5000/

```



\### Output



```json

{

&#x20;   "message": "Flask CRUD API is running"

}

```



\### Result



✅ Flask API is running successfully.



\---



\## 2. Create User



\### Request



\*\*POST\*\*



```text

http://127.0.0.1:5000/users

```



\### Request Body



```json

{

&#x20;   "name": "Sathya",

&#x20;   "email": "sathya@gmail.com"

}

```



\### Output



```json

{

&#x20;   "id": 3,

&#x20;   "message": "User created successfully"

}

```



\### Result



✅ User created successfully.



\---



\## 3. Get All Users



\### Request



\*\*GET\*\*



```text

http://127.0.0.1:5000/users

```



\### Output



```json

\[

&#x20;   {

&#x20;       "id": 2,

&#x20;       "name": "Sai",

&#x20;       "email": "sai@gmail.com"

&#x20;   }

]

```



\### Result



✅ All users retrieved successfully.



\---



\## 4. Get User by ID



\### Request



\*\*GET\*\*



```text

http://127.0.0.1:5000/users/3

```



\### Output



```json

{

&#x20;   "id": 3,

&#x20;   "name": "Sathya",

&#x20;   "email": "sathya@gmail.com"

}

```



\### Result



✅ Individual user retrieved successfully.



\---



\## 5. Update User



\### Request



\*\*PUT\*\*



```text

http://127.0.0.1:5000/users/3

```



\### Request Body



```json

{

&#x20;   "name": "Sathya Sri",

&#x20;   "email": "sathyasri@gmail.com"

}

```



\### Output



```json

{

&#x20;   "message": "User updated successfully"

}

```



\### Result



✅ User updated successfully.



\---



\## 6. Delete User



\### Request



\*\*DELETE\*\*



```text

http://127.0.0.1:5000/users/3

```



\### Output



```json

{

&#x20;   "message": "User deleted successfully"

}

```



\### Result



✅ User deleted successfully.



\---



\# 🧪 CRUD Testing Summary



The following CRUD operations were successfully tested using \*\*Postman\*\*:



| Test           | Method | Result       |

| -------------- | ------ | ------------ |

| Create User    | POST   | ✅ Successful |

| Get All Users  | GET    | ✅ Successful |

| Get User by ID | GET    | ✅ Successful |

| Update User    | PUT    | ✅ Successful |

| Delete User    | DELETE | ✅ Successful |



\---



\# 🐘 PostgreSQL Database



This project uses \*\*PostgreSQL\*\* as the database.



\### Database Configuration



```text

Database: flaskdb

Username: postgres

Port: 5432

```



The PostgreSQL database runs inside a Docker container.



\### Database Table



The application uses a `user` table containing:



```text

id

name

email

```



Example database record:



```text

id | name | email

\---|------|----------------

2  | Sai  | sai@gmail.com

```



\---



\# 🐳 Docker Setup



The project uses Docker Compose to run both:



1\. Flask application

2\. PostgreSQL database



\### Start the Application



```bash

docker compose up --build

```



\### Check Containers



```bash

docker compose ps

```



\### Successful Docker Output



```text

NAME                   SERVICE   STATUS

flask-crud-api-db-1    db        Up (healthy)

flask-crud-api-web-1   web       Up

```



\### Ports



```text

Flask       → 5000

PostgreSQL  → 5432

```



\### Stop the Application



```bash

docker compose down

```



\### Start Again



```bash

docker compose up

```



\---



\# 🏗️ Docker Architecture



```text

&#x20;                Flask CRUD API

&#x20;                      |

&#x20;                      |

&#x20;                Docker Compose

&#x20;                  /        \\

&#x20;                 /          \\

&#x20;            Flask Web     PostgreSQL

&#x20;            Container      Container

&#x20;               |               |

&#x20;            Port 5000       Port 5432

&#x20;               |

&#x20;            REST API

&#x20;               |

&#x20;            Postman

```



\---



\# 📦 Installation



\## Prerequisites



Install the following:



\* Python

\* Docker Desktop

\* Git

\* Postman



\---



\## Run Using Docker



Clone the repository:



```bash

git clone https://github.com/saisathyasrigannu999-oss/flask-crud-api.git

```



Go to the project directory:



```bash

cd flask-crud-api

```



Build and start the containers:



```bash

docker compose up --build

```



Open the API:



```text

http://127.0.0.1:5000/

```



\---



\# 💻 Run Without Docker



Install the required Python packages:



```bash

pip install -r requirements.txt

```



Run the Flask application:



```bash

python app.py

```



However, Docker Compose is recommended because it manages both the Flask application and PostgreSQL database.



\---



\# 🔐 Database Connection



The Flask application connects to PostgreSQL using:



```text

postgresql://postgres:postgres@db:5432/flaskdb

```



Here:



```text

postgres   → PostgreSQL username

postgres   → PostgreSQL password

db         → Docker PostgreSQL service name

5432       → PostgreSQL port

flaskdb    → Database name

```



\---



\# 📡 REST API Flow



```text

Client / Postman

&#x20;      |

&#x20;      ↓

&#x20;  Flask API

&#x20;      |

&#x20;      ↓

SQLAlchemy ORM

&#x20;      |

&#x20;      ↓

&#x20;PostgreSQL

&#x20;      |

&#x20;      ↓

&#x20;  Database

```



\---



\# 📚 Learning Outcomes



Through this project, I learned:



\* How to build REST APIs using Flask

\* How CRUD operations work

\* How to use Flask-SQLAlchemy

\* How to connect Flask with PostgreSQL

\* How SQLAlchemy ORM works

\* How to containerize an application using Docker

\* How to manage multiple services using Docker Compose

\* How to test REST APIs using Postman

\* How to use Git for version control

\* How to upload and manage projects using GitHub



\---



\# 🎯 Project Highlights



\* ✅ RESTful API architecture

\* ✅ Complete CRUD functionality

\* ✅ PostgreSQL database integration

\* ✅ SQLAlchemy ORM

\* ✅ Dockerized Flask application

\* ✅ Docker Compose

\* ✅ Postman API testing

\* ✅ Git version control

\* ✅ GitHub repository

\* ✅ Professional project documentation



\---



\# 👩‍💻 Author



\*\*Sai Sathya Sri\*\*



\*\*B.Tech – Computer Science Engineering (Data Science)\*\*



\---



\## 🔗 GitHub Repository



\[Flask CRUD REST API](https://github.com/saisathyasrigannu999-oss/flask-crud-api)



\---



\## ⭐ Conclusion



This project demonstrates the development of a complete backend CRUD REST API using Flask and PostgreSQL, with Docker-based deployment and Postman-based API testing.
It provides practical experience in backend development, database integration, API development, containerization, testing, and version control.

Output:
<img width="1917" height="851" alt="Image" src="https://github.com/user-attachments/assets/f7fbb6fd-356c-457f-948d-a0841260e9fb" />

