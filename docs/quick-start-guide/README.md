## ❯ Quick Start Guide

### Clone the project

Change the current working directory to the location where you want the cloned project to be:

```
cd ~/workspace
```

Clone the project by running the following command:

```
git clone git@github.com:Robinyo/hapi-fhir-jpaserver-starter.git
cd ~/workspace/hapi-fhir-jpaserver-starter
``` 

### Docker Compose

#### Build

To build the project:

```
docker compose -f docker-compose-fhir-au.yml build
```

#### Run

With a single command, you can create and start all the services:

```
docker compose -f docker-compose-fhir-au.yml up
```

Navigate to the **Welcome** page: 

```
http://localhost:8080
```

You should see something like:

<p align="center">
  <img src="./welcome.png" alt="Welcome page"/>
</p>

To stop the services:

```
docker compose -f docker-compose-fhir-au.yml stop
```

To restart the services:

```
docker compose -f docker-compose-fhir-au.yml up
```

To remove the services:

```
docker compose -f docker-compose-fhir-au.yml down
```

To remove the data volume:

```
docker volume rm hapi-fhir-jpaserver-starter_postgres_data
```

