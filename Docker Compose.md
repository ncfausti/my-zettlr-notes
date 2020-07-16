20200611120541

### Docker Compose

a tool that is used to control and send commands to services that are defined in docker-compose.yml file.

For example, if I wanted to run a database migration on a django project that is running inside of a container I can use the following command:

    docker-compose run web python manage.py migrate

Uses a Dockerfile [[20200611134708]] and docker-compose.yml file.

Other commands: `build, up, down`

Example docker-compose.yml file that defines two services: The`db`service and the`web`service:

`version: '3'
    
  services:
    db:
      image: postgres
      environment:
        - POSTGRES_DB=postgres
        - POSTGRES_USER=postgres
        - POSTGRES_PASSWORD=postgres
    web:
      build: .
      command: python manage.py runserver 0.0.0.0:8000
      volumes:
        - .:/code
      ports:
        - "8000:8000"
      depends_on:
        - db`

[https://docs.docker.com/compose/django/](https://docs.docker.com/compose/django/)

#code #docker 