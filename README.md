# Facultative's quiz

## Steps to deploy the app on Docker containers

### React Application

* Run "npm i" to download all applicacation dependencies 

* Run "npm run build" putting before the value for environment variable like this: **REACT_APP_API_URL=http://localhost:9000/api/todos**
    
    This is beacause our application needs to know which will be API URL to make queries them. Once ready go follow.

### Running up docker compose

    all services came preconfigured, therefore, this is only run the command "docker-compose up" inside folder contain docker-compose.yml file.

    Once all services are running up, goes to next step. 

### Database creation

    The database doesn't came with autocreation by default, so, we must create it manually.

#### steps:
* Run "docker ps" command to list all running containers. 

* we'll take and copy mssql container ID

* next we go to run the command "docker exec -it <container-Id/Container-name> /opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P <your_password>"

    A bash terminal will open and we must create the database with the name writted on docker compose manifes, in this case is "todosDB", and to perform this we'll use the script "DATABASE_CREATIOS.sql attached in this repository. 

Now we should look our application running on port 3000 in [localhost](http://localhost:3000). 

