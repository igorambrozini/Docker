## Project.1_Creating MySQL database in Docker (Linux/Windows)
Docker documentation: https://docs.docker.com/

### 1) Downloading Docker Desktop
Download last version at: https://www.docker.com/products/docker-desktop/

### 2) Install Docker Desktop
Follow steps until installation is complete.

### 3) Choose Docker Image
Go and sign in to https://hub.docker.com/ and search for mysql (official image)

### 4) Creating and running container in Docker
#### Open prompt and type:

Check if docker is installed and version:
> docker -v

Download and install docker image:
>  docker pull mysql

Creating container mysql:
> docker run -p 3306:3306 --name mysql_database -e MYSQL_ROOT_PASSWORD=root -d mysql

*-p to set port 3306  
-- name to set name musql_database  
MYSQL_ROOT_PASSWORD to set password = root  
mysql (docker image name)*

Check if container mysql is running:
> docker ps

Go to Docker Desktop and verify it is running.

### 5) Check connection using a DBMS compatible with mysql like Workbench mysql

Create a new database connection using:  
connection method: TCP/IP  
hostname: 127.0.0.1  
port: 3306  
username: root  
password: root

### 6) Docker Basic commands

Create a container:
> docker run [imagem name]

Download a image (to create containers)
> Docker pull (parameter)

Start container:
> docker start mysql_database

Stop container:
> docker stop mysql_database

Check all cointainers created:
> docker ps

Create a new image using a Dockerfile (path or URL, especific parameters)
> docker build [OPTIONS] PATH | URL | –

Execute a command in a running container:
> docker exec [opções] CONTAINER COMMAND [ARGUMENTS]
