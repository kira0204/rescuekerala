# Kerala Rescue

Website for coordinating rehabilitation of people affected in the 2018 Kerala Floods

## Contributions

It's great that we all are coming together to help this website, every helping hand is required and appreciated, but before you make any contribution, below are some points that you should keep in mind.

- Select an issue that you want to work upon and comment on the same so that no other person takes up the same issue
- If the issue your PR is solving is not mentioned in the issues tab, first open the issue and then solve it so that other people know what you are working upon and hence we reduce the number of duplicates.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

You will need to have following softwares in your system

- Python 3
- Postgres
- git

### Installing

Setting up development environment

create database and user in postgres for kerala rescue and give privileges

```
psql user=postgres
Password: 
psql (10.4 (Ubuntu 10.4-0ubuntu0.18.04))
Type "help" for help.

postgres=# CREATE DATABASE rescuekerala;
CREATE DATABASE
postgres=# CREATE USER rescueuser WITH PASSWORD 'password';
CREATE ROLE
postgres=# GRANT ALL PRIVILEGES ON DATABASE rescuekerala TO rescueuser;
GRANT
postgres=# \q

```
Clone the repo
```
git clone https://github.com/IEEEKeralaSection/rescuekerala.git
cd rescuekerala
```

Copy sample environment file and configure it as per your local settings

```
cp .env.example .env
```

Install dependencies

```
pip3 install -r requirements.txt
```

Run Database migrations

```
python3 manage.py migrate
```

Setup staticfiles
```
python3 manage.py collectstatic
```

Run the server

```
python3 manage.py runserver
```
Now open localhost:8000 in the browser
