# Goxygen

## Environment setup

You need to have [Go](https://golang.org/),
[Node.js](https://nodejs.org/),
[Docker](https://www.docker.com/), and
[Docker Compose](https://docs.docker.com/compose/)
(comes pre-installed with Docker on Mac and Windows)
installed on your computer.

Verify the tools by running the following commands:

```sh
go version
npm --version
docker --version
docker-compose --version
```

If you are using Windows you will also need
[gcc](https://gcc.gnu.org/). It comes installed
on Mac and almost all Linux distributions.


# Application creation

Documentation URL [For goxygen](https://github.com/Shpota/goxygen)


# Supported Technologies

```sh
Front End -	Angular-Reac-Vue
Back End  - Go
Database  - MongoDB-MySQL-PostgreSQL
```

# Cmd to create the application

```sh
go run github.com/shpota/goxygen@latest init --frontend vue --db postgres my-app
```

# Possible combination that you can create with Goxygen

The --frontend flag accepts angular, react and vue. The --db flag accepts mongo, mysql and postgres.

# Database configuration 
Make sure you set all these details for your database

## Postgres

```sh
 dev_db:
    environment:
      POSTGRES_PASSWORD: your postgres password
      POSTGRES_USER: postgres username
      POSTGRES_DB: postgres dbname
      POSTGRES_PORT:5432

SAMPLE DB CONNECTION STRING:
    "postgresql://" + localhost + ":{portnumber}/{databasename}" + "?user={username}&sslmode=disable&password=" + {dbpassword}
      
```


## Mysql

```sh

dev_db:
    environment:
      MYSQL_PASSWORD: your mysql password
      MYSQL_USER: mysql username
      MYSQL_DATABASE: mysql dbname
      POSTGRES_PORT:3306

SAMPLE DB CONNECTION STRING:
    "{username}:" + {dbpassword} + "@tcp(" + localhost + ":{portnumber})/tech"  

```

## Mongo

In mongo Db make sure you change your collection name with the collection you create in the database

```sh
dev_db:
    environment:
      MONGO_USER: mongo username
      MONGO_INITDB_DATABASE: tech
      POSTGRES_PORT:27017

SAMPLE DB CONNECTION STRING:
    "mongodb://" + localhost + ":{portnumber}"

```

# Database data

each app created will have a script file named  
## init-db.js 

use that script file to create the sample data in the database

Documentation URL [For goxygen](https://github.com/Shpota/goxygen)


# Go Backend Api GET URl

 * http://localhost:8080/api/technologies


# Docker configuration settings for container deplowment

Step 1 : Install Docket desktop to create containet in respective docker application . Docker installation instruction [Site](https://docs.docker.com/engine/install/).

Step 2 : Follow the instruction in the Document to allow access to docker user in the particular system 

 * If you haven’t already downloaded the installer (Docker Desktop Installer.exe), you can get it from Docker Hub. It typically downloads to your Downloads folder, or you can run it from the recent downloads bar at the bottom of your web browser.

 * When prompted, ensure the Enable Hyper-V Windows Features or the Install required Windows components for WSL 2 option is selected on the Configuration page.

 * Follow the instructions on the installation wizard to authorize the installer and proceed with the install.

 * When the installation is successful, click Close to complete the installation process.

 * If your admin account is different to your user account, you must add the user to the docker-users group. Run Computer Management as an administrator and navigate to Local Users and Groups > Groups > docker-users. Right-click to add the user to the group. Log out and log back in for the changes to take effect.

step 3 : Follow the induvidual docker instruction fro further deploy in the docker

# Thank you

