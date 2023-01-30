# banking
##### Run `./start.sh` to download the dependencies and run the the application

To run the application, you have to define the environment variables, default values of the variables are defined inside `start.sh`

- SERVER_ADDRESS    `[IP Address of the machine]`
- SERVER_PORT       `[Port of the machine]`
- DB_USER           `[Database username]`
- DB_PASSWD         `[Database password]`
- DB_ADDR           `[IP address of the database]`
- DB_PORT           `[Port of the database]`
- DB_NAME           `[Name of the database]`

# mysql database
You can use any one of the following procedure to make a database instance, and make the changes to your `start.sh` file accordingly 
1. `docker-compose.yml` file. This contains the init script to generate and tables and insert the default data. You just need to bring the container up

    To start the docker container, run the `docker-compose up` inside the `resources/docker` folder
 
2. `resources/database.sql` this contains the SQL for generating the tables. In case you dont want to use the docker-compose file you can use this file to generate tables and insert the default data

# mocks generator
`./generate-mocks.sh`

# run unit tests
  `./run-tests.sh`

```shell
  docker exec -it mysql /bin/bash

  mysql -uroot -pcodecamp  
```

#### connect to db - banking and invoke command - "SHOW tables"
```shell
  docker exec -it mysql   mysql -uroot -pcodecamp banking -e "SHOW tables"
```

https://geshan.com.np/blog/2022/02/mysql-docker-compose/
https://medium.com/@chrischuck35/how-to-create-a-mysql-instance-with-docker-compose-1598f3cc1bee

Short Project Structure:

  app/
  domain/
  dto/
  mocks/
    domain/
    service/
  resources/
    docker/
  service/

http://localhost:8000/customers
