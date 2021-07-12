## About this project

RESTful API, using Test-Driven Development. The API itself will follow RESTful design principles, using the basic HTTP verbs: GET, POST, PUT, and DELETE.

## Development Requirements

*  [Docker](https://docs.docker.com/get-started/).
*   [Docker](https://docs.docker.com/compose/gettingstarted/).

## Local development

* Build the image

`docker-compose build`

*  Once the build is done, fire up the container in detached mode:

`docker-compose up -d`

* Now you can open your browser and interact with these URLs:

Navigate to http://localhost:8009/ping to check the app is running.

* Bring down the development containers

`docker-compose down -v`

### Aditional commands

* Run the migrations:

`docker-compose exec movies python manage.py migrate --noinput`

* Run the tests:

`docker-compose exec movies pytest`