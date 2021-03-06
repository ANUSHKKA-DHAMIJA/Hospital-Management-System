# Hospital Management System(Without Interface)

A system written in Python which connects to MySQL and can be used to manage hospital work.

## Installation

Install Docker and start docker engine. The 'docker-compose.yml' when run as shown below will get two docker containers up and running, one with MySQL and one with Python.

```bash
docker-compose up -d
```
The docker containers and their IDs can be viewed by using below cmd.

```bash
docker ps
```
We can access the command prompt of the container using container ID.

```bash
docker exec -it <containerID> bash
```
The two containers communicate between one another using MySQL Connector and the password is entered wherever required using stdiomask library which displays asterisks '*' as password is entered unlike python's built-in getpass library which hides what is entered. Both can be installed in the Python container where we run our script.

```bash
pip install mysql-connector-python
```
```bash
pip install stdiomask
```
In the MySQL container, we can start MySQL using the below cmd.

```bash
mysql -u <user> -p <password>
```

## Usage

The 'Code' folder contains the file "system.py" which has our main code and can be executed using below command in the Python container.

```bash
python system.py
```