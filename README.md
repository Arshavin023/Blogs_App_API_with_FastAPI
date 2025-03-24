# FastAPI Development for BlogPost App
## Overview
The repository demonstrates basics of API development with FastAPI.

# Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Deployment](#deployment)
- [License](#license)
- [Contributing](#contributing)  
- [Authors & Acknoledgements](#authors_and_acknowledgments)

## Introduction <a name="introduction"></a>
This repository demonstrates steps to be followed when developing an API with FastAPI for a social media blog platform. It leverages the psycopg2, fastapi and sqlalchemy libraries for functions.

## Installation <a name="installation"></a>
#### Prerequisites <a name="prerequisites"></a>
Before running the File Ingestion Process, ensure you have the following prerequisites installed:
- Python 3.x
- PostgreSQL database

## Configuration <a name="configuration"></a>
Generate and save secret key with 
```
openssl rand -hex 32
```
Create database with name "blogpost_db" and username "blogpost_admin"
Create .env database_credentials file, fill in the info and store in the home directory
```
cd ~ && nano /home/server_user/.env
```
DATABASE_HOSTNAME=localhost
DATABASE_PORT=5432
DATABASE_PASSWORD=admin123!
DATABASE_NAME=blogpost_db
DATABASE_USERNAME=blogpost_admin
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

## Usage <a name="usage"></a>
Clone repository
```
mkdir blogpost_API_development && cd blogpost_API_development
git clone https://github.com/Arshavin023/Blogs_App_API_with_FastAPI.git .
```
Create and activate virtual environment
```
virtualenv venv 
source venv/bin/activate
```
Install the packages in requirements.txt:
```
pip install -r requirements.txt
```
Initialize and Perform Alembic migrations
``` 
alembic init alembic
alembic upgrade head
```

Test app
``` 
uvicorn --host 127.0.0.1 app.app:app
```

## Deployment <a name="deployment"></a>
Build app as a service and deploy in /etc/systemd/system

## License <a name="license"></a>
- MIT License

## Authors & Acknowledgements <a name="authors_and_acknowledgments"></a>
- Uche 



