\# Flask CRUD REST API



A simple and scalable CRUD (Create, Read, Update, Delete) REST API built using Python Flask, Flask-SQLAlchemy, PostgreSQL, and Docker.



This project demonstrates how to build a backend REST API, connect it to a PostgreSQL database, containerize the application using Docker, and test the API using Postman.



\## 🚀 Project Overview



The Flask CRUD REST API allows users to perform basic database operations through REST API endpoints.



The application uses Flask as the backend framework, SQLAlchemy as the ORM, PostgreSQL as the database, and Docker for containerization.



\## 🛠️ Technologies Used



\* Python

\* Flask

\* Flask-SQLAlchemy

\* PostgreSQL

\* Docker

\* Docker Compose

\* Postman

\* Git

\* GitHub



\## ✨ Features



\* Create a new user

\* Retrieve all users

\* Retrieve a user by ID

\* Update an existing user

\* Delete a user

\* PostgreSQL database integration

\* SQLAlchemy ORM

\* Docker containerization

\* Docker Compose for managing Flask and PostgreSQL

\* REST API testing using Postman



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



\## 🔄 CRUD Operations



| Operation | HTTP Method | Endpoint      | Description             |

| --------- | ----------- | ------------- | ----------------------- |

| Create    | POST        | `/users`      | Create a new user       |

| Read All  | GET         | `/users`      | Retrieve all users      |

| Read One  | GET         | `/users/<id>` | Retrieve a user by ID   |

| Update    | PUT         | `/users/<id>` | Update an existing user |

| Delete    | DELETE      | `/users/<id>` | Delete a user           |



\## 🌐 API Endpoints



\### 1. Check API Status



\*\*GET\*\*



```text

http://127.0.0.1:5000/

```



Response:



```json

{

&#x20;   "message": "Flask CRUD API is running"

}

```



\### 2. Create User



\*\*POST\*\*



```text

http://127.0.0.1:5000/users

```



Request Body:



```json

{

&#x20;   "name": "Sai",

&#x20;   "email": "sai@gmail.com"

}

```



Example Response:



```json

{

&#x20;   "message": "User created successfully",

&#x20;   "id": 2

}

```



\### 3. Get All Users



\*\*GET\*\*



```text

http://127.0.0.1:5000/users

```



Example Response:



```json

\[

&#x20;   {

&#x20;       "id": 2,

&#x20;       "name": "Sai",

&#x20;       "email": "sai@gmail.com"

&#x20;   }

]

```



\### 4. Get User by ID



\*\*GET\*\*



```text

http://127.0.0.1:5000/users/2

```



\### 5. Update User



\*\*PUT\*\*



```text

http://127.0.0.1:5000/users/2

```



Request Body:



```json

{

&#x20;   "name": "Sai Sri",

&#x20;   "email": "saisri@gmail.com"

}

```



Example Response:



```json

{

&#x20;   "message": "User updated successfully"

}

```



\### 6. Delete User



\*\*DELETE\*\*



```text

http://127.0.0.1:5000/users/2

```



Example Response:



```json

{

&#x20;   "message": "User deleted successfully"

}

```



\## 🐘 Database



This project uses PostgreSQL as the relational database.



Database configuration:



```text

Database: flaskdb

Username: postgres

Port: 5432

```



The PostgreSQL database runs inside a Docker container.



\## 🐳 Docker Setup



The project uses Docker Compose to run both the Flask application and PostgreSQL database.



\### Start the Application



```bash

docker compose up --build

```



The API will be available at:



```text

http://127.0.0.1:5000/

```



\### Check Running Containers



```bash

docker compose ps

```



\### Stop the Application



```bash

docker compose down

```



\### Start Again



```bash

docker compose up

```



\## 🧪 API Testing



The API was tested using Postman.



The following operations were successfully tested:



\* POST - Create User

\* GET - Retrieve Users

\* GET by ID - Retrieve Individual User

\* PUT - Update User

\* DELETE - Delete User



\## 📦 Installation Without Docker



If you want to run the Flask application locally, install the required Python packages:



```bash

pip install -r requirements.txt

```



Then run:



```bash

python app.py

```



However, Docker Compose is recommended because it automatically manages the Flask application and PostgreSQL database.



\## 🔐 Environment and Configuration



The application uses PostgreSQL with the following connection:



```text

postgresql://postgres:postgres@db:5432/flaskdb

```



The hostname `db` refers to the PostgreSQL service defined in `docker-compose.yml`.



\## 📌 Learning Outcomes



Through this project, I learned:



\* Building REST APIs using Flask

\* Implementing CRUD operations

\* Working with Flask-SQLAlchemy

\* Connecting Flask with PostgreSQL

\* Using SQLAlchemy ORM

\* Containerizing applications using Docker

\* Managing multiple services using Docker Compose

\* Testing REST APIs using Postman

\* Using Git and GitHub for version control



\## 👩‍💻 Author



\*\*Sai Sathya Sri\*\*



B.Tech – Computer Science Engineering (Data Science)



\## ⭐ Project Highlights



\* RESTful API architecture

\* PostgreSQL database integration

\* SQLAlchemy ORM

\* Dockerized application

\* CRUD functionality

\* Postman API testing

\* GitHub version control



