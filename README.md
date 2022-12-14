<h1 align="center">OpenClassrooms Project 12</h1>

# Develop a Secure Back-End Architecture Using Django ORM
> This is my project No. 12 for OpenClassrooms where I had to create a Secure Back-End Architecture Using Django ORM. The API/application is made for Epic Events, a boutique event management and consulting firm. The Django application needs to deliver a set of secure API endpoints using the Django REST framework & ORM (with a PostgreSQL database) to support CRUD (create, read, update, and delete) operations on the various CRM objects. Additionally I needed to create a simple front-end using the Django admin site, which will allow authorized users to maintain the application, access all models, and verify database setup.

## Table of Contents
* [General Info](#general-information)
* [Postman documentation](#postman-documentation)
* [Prerequisite](#prerequisite)
* [Setup](#setup)


## General Information
- Set of secure API endpoints using the Django REST framework & ORM (with a PostgreSQL database)
- Front-end using the Django admin site
- Authentication via JSON Web Tokens (JWTs)

## Postman documentation
```Bash
https://documenter.getpostman.com/view/19314829/VUjTihoX
```

## Prerequisite
- [Python 3.10.4](https://www.python.org/ "Python") is installed
- [PostgreSQL](https://www.postgresql.org/download/ "PostgreSQL") is installed

## Setup
1. Clone the repository

```Bash
git clone https://github.com/aschickhoff/OCproject12
```

2. Go to your work directory and access the project folder

## for Windows
3. Create a virtual environment
```Bash
python -m venv env
```

4. Activate the virtual environment
```Bash
.\env\Scripts\activate
```

## for Linux
3. Create a virtual environment
```Bash
python3 -m venv env
```

4. Activate the virtual environment
```Bash
source env/bin/activate 
```

## Packages
5. Install needed packages

```Bash
pip install -r requirements.txt
```

## Database
6. Create the database SQL shell (psql)
```Bash
CREATE USER admin WITH ENCRYPTED PASSWORD "###dbepicevents";
```
```Bash
CREATE DATABASE epicevents;
```
```Bash
GRANT ALL PRIVILEGES ON DATABASE epicevents TO admin;
```

7. Create file .env and paste:
```Bash
SECRET_KEY = ""
DEBUG = True
DBUSER = "admin"
DBPASSWORD = "###dbepicevents"
```

Fill SECRET_KEY with received key

8. Migrations
```Bash
python manage.py migrate
```

## Superuser
9. Create superuser
```
python manage.py createsuperuser
```

## Start the server
10. Launch the Django server
```Bash
python manage.py runserver
```
