# **MeetMeat Project - Back-office**

Welcome to the MeetMeat project, back-office branch.  
In this project, each service has its own repository.

- [Back-office](https://github.com/Cyrilloche/T-ESP-900-backoffice)
- [Backend](https://github.com/Cyrilloche/T-ESP-900-backend)
- [Mobile](https://github.com/Cyrilloche/T-ESP-900-mobile)

## Back-office

The back-office project is a web application based on Vue.js.

## For developers in charge of developing the project

### Project structure

This project has two main folders:

``` bash
├───backoffice # directory containing the source code
└───docker     # directory containing the Docker setup
```

> [!IMPORTANT]  
> Please do not modify this structure during development.

### Project creation

As this is a Vue.js project, you must initialize the project inside the `/backoffice` directory.  
Run the following commands to create the **MeetMeat Back-office project**.

#### Initialize the project

``` bash
cd ./backoffice
npm create vite@latest . -- --template vue

# Select Vue
# Select Official Vue Starter
# Set the package name
package.json
# Select your needed dependencies
# Select None for experimental features
```

#### Install Node modules

``` bash
npm install
```

#### Environent variables
Following the `.env.example` file, please create a `.env.dev` file with your secrets and credentials.

>[!IMPORTANT]
>This file will be not push. Please update the `.env.example` with the new secrets and credentials, and advice your teammate. 

## Run the application

### Development

Run the following command to start the Docker container in development mode.  
This setup includes hot reload on save.

```bash
# Run this command from the root of the project
docker compose -f ./docker/docker-compose.dev.yml --env-file ./docker/.env.dev up -d --build
```

The application should be run on [localhost:5173](http://localhost:5173/).

### Production

Run the following command to start the Docker container in production mode.  

```bash
# Run this command from the root of the project
docker compose -f ./docker/docker-compose.prod.yml --env-file ./docker/.env.prod up -d --build
```