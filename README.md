# docker-nodejs-app

# Clone the repository to your work machine
$ git clone YOUR_REPOSITORY_URL
$ cd YOUR_REPOSITORY_NAME

# Express Application
$ npx express-generator --no-view addressbook
$ cd addressbook
$ npm install

# Configuring the Database
$ npm install --save pg sequelize

# Install JavaScript testing library
$ npm install --save-dev jest

# Setting Up PM2
$ npm install --save pm2
$ npm run pm2

# Running Postgres With Docker
$ docker run -it -e "POSTGRES_HOST_AUTH_METHOD=trust" -p 5432:5432 postgres

# Database running, open a new terminal and execute the migrations to create the table
$ npm run migrate
$ npm run pm2

# Database tests
$ npm run test

# Creating a Dockerfile
$ touch Dockerfile
$ touch .dockerignore

# Bundling and Running the Docker Container
$ docker build -t addressbook .
$ docker run -it -p 3000:3000 addressbook

# Docker Compose 
$ touch docker-compose.yml

# Stop the PostgreSQL container
$ docker ps

# Start Docker Compose and run the tests
$ docker-compose run addressbook npm test

# Start the app and use curl to test the endpoint
$ docker-compose up -d
$ curl -w "\n" \
       -X PUT \
       -d "firstName=Bobbie&lastName=Draper" \
       localhost:3000/persons
$ curl -w "\n" localhost:3000/persons/all

--------------------------------------------------------
# Commit chnages
$ git add -A
$ git commit -m "initial commit"
$ git push origin master


