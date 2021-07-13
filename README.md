## About this project

RESTful API, using Test-Driven Development. The API itself will follow RESTful design principles, using the basic HTTP verbs: GET, POST, PUT, and DELETE.

Practices to create each endpoint with TDD:
1. write a test
2. run the test, to ensure it fails (**red**)
3. write just enough code to get the test to pass (**green**)
4. **refactor** (if necessary)

## Development Requirements

*  [Docker](https://docs.docker.com/get-started/).
*   [Docker Compose](https://docs.docker.com/compose/gettingstarted/).

## Local development

* Build the image

`docker-compose build`

*  Once the build is done, fire up the container in detached mode:

`docker-compose up -d`

* Now you can open your browser and interact with these URLs:

Navigate to http://localhost:8009/ping to check the app is running.

* Bring down the development containers

`docker-compose down -v`

## Aditional commands

#### Migrations

* Create the migration:

`docker-compose exec movies python manage.py makemigrations`

* Run the migrations:

`docker-compose exec movies python manage.py migrate --noinput`


#### Tests

* Run the tests:

`docker-compose exec movies pytest`

* Run specific tests:

`docker-compose exec movies pytest -k hello_world`