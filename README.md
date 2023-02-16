# Workshop_Pyramid

## Introduction

Welcome to our Workshop, today we will see how to create a to-do list application web using [Python](https://python.org/) with the framework [Pyramid](https://trypyramid.com/) and the database [SQLite](https://www.sqlite.org/index.html).\
We hope that you will enjoy and learn as much as you can during this workshop ! :)

---
## Prerequisites

### **What we need ?**
For this workshop you will need to have **Python** installed on your computer. If it's not already done, you can find the installation [here](https://www.python.org/downloads/).
We also need to install a database, in our case we will use [SQLite](https://www.sqlite.org/download.html), you can download it from the package manager of your machine. (We advice you to download the sqlite browser to have an user interface)


### **How to build** :
You have to configure an environment. Then let's create a virtual environment:
```sh
    python3 -m venv venv
```

Once your virtual env is created, you can install the required packages provide by the requirements.txt file:
```sh
    venv/bin/pip install -r requirements.txt
```

Now you can launch your web application:
```sh
    venv/bin/python3 main.py
```
---
---
## **DOCUMENTATION /!\\**
- _You will find all the documentation you need by clicking [here](https://docs.pylonsproject.org/projects/pyramid/en/latest/index.html) or with the following link: https://docs.pylonsproject.org/projects/pyramid/en/latest/index.html_

---
---

## __STEP 1__ : **_Create a server_**
    Let's create a server that will listen to the port 8000 on your local machine.
    You have to create a WSGI application and then create an object that can launch your web server.

---
## __STEP 2__ : **_Create a basic route_**
    Create a route to "/home" and print "hello world" as title using a function.
    For this we will configure details and set parameters to your route using the function Configurator provided by the framework Pyramid

---
## __STEP 3__ : **_Connect your database_**
    Connect your sqlite3 database to your pyramid server.
    You have to create a function and use the path of the file "my.db" gived in the repository.

---
## __STEP 4__ : **_Make SQL Query to get your data_**
    With your connection to the database, make an SQL Query to SELECT the "Users" table and print it in order to test if you get it all.

---
## __STEP 5__ : **_Register_**
    For the registration, you have to :
        - Get the data from the request's parameters (username and password)
        - Check if the username and the password are not already used
        - If not, put the user to the "Users" table
        - Redirect the user  to the login page

## __STEP 6__ : **_Login_**
    For the login, you have to :
        - Get the data from the request's parameters (username and password)
        - Check if the user is in the database
        - Print welcome "username"

---
## __STEP 7__ : **_Logout_**
    The logout is pretty simple, you just have to redirect the user to the home page.

---
## **BONUSES** :
### **BONUS 1 : _Use a Token_**
    You can make a SHA256 token from the username and the password to secure the communication with the front (in the case of a real application)

### **BONUS 2 : Dockerisation**
    You can create a Dockerfile to generate an image of your web application.
    Next you can create a docker-compose in order to run your web application into a container.
