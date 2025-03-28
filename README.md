I made this so you can run my Portfolio 2023 front-end, back-end and tests in containers in the same network. You will have to:

- Clone this repository to your local machine.

- Then clone to the root directory of this repository the front-end, back-end and tests repositories:

  - portfolio-2023
  - portfolio-server
  - portfolio-2023-RF-tests

- Create a new file named 'initdb.d/init.sql' also to the root directory. This is the file you should write your SQL initialization script.

- Create a .env file to the root directory and add the following fields to it. Replace the example values with real values:

  REACT_APP_NASA_API_TOKEN=[your nasa_api token]  
  DATABASE=classicmodels  
  PORT=3001  
  DBUSER=node_client  
  DBPORT=3306  
  DB_RANDOM_TABLE_NAME=customers  
  DB_RANDOM_TABLE_NAME_JSON_FILE=table-content  
  FRONT_END_URL=http://localhost:3000  
  BROWSER_OPENING=small-width_opening  
  EMPTY_TABLE=empty_table  
  FILLED_TABLE=customers
    
- Create a file 'mysql_root_password.txt' to the root directory. Write to this file only the root password to the mysql database.

- Create a file 'password.txt' also to the root directory. Write to this file only the password for the DBUSER.

- Navigate to front-end and back-end directories and then run 'npm install' command to install dependencies to them.

If you want to build the images locally, then you have to comment out the image-line from each service in the docker-compose file and also uncomment the build-line. Use the command 'docker-compose up' to create the containers.

Copyright 2025 Tapani Voutilainen

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
