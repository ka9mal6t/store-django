<div align="center">

# Store Server
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](LICENSE) 
</div>

# Table of contents
1. [Tech Stack](#Stack)
2. [Features](#Features)
3. [Run Locally](#run)
4. [Feedback](#Feedback)
5. [License](#License)
<div id="Stack">

## Stack:

- [Python](https://www.python.org/downloads/)
- [PostgreSQL](https://www.postgresql.org/)
- [Redis](https://redis.io/)
</div>
<div id="Features">

## Features

- Authorizing user
- Registration new user
- Buying goods
- Goods tracking
- Payment for goods
- Data hashing for speedup
</div>

<div id="run">

## Run Locally
Firstly, create and activate a new virtual environment:
   ```bash
   python -m venv ../venv
   source ../venv/bin/activate
   ```
   
Install packages:
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
   
Run project dependencies, migrations, fill the database with the fixture data etc.:
   ```bash
   ./manage.py migrate
   ./manage.py loaddata <path_to_fixture_files>
   ./manage.py runserver 
   ```
   
Run [Redis Server](https://redis.io/docs/getting-started/installation/):
   ```bash
   redis-server
   ```
   
Run Celery:
   ```bash
   celery -A store worker --loglevel=INFO
   ```
</div>
<div id="Feedback">

## Feedback

If you have any feedback, please reach out to us at vladimyr.kilko@gmail.com
</div>

<div id="License">

## License

[GPLv3 License](LICENSE)
</div>