20200622181415

### Docker Exec

To log into my running docker container I first need to make sure it is built and running:

docker-compose [[20200611120541]] -f <path/to/.yml file> build
docker-compose <path/to/.yml file up
docker ps

Using the COTNTAINER ID run:

docker exec -t -i <CONTAINER_ID_HERE> bash

-t and -i are for a pseudo TTY and interactive mode, respectively.

This above code will put me into the container where I can run commands as usual.

#operatingsystems #os #sysadmin #docker #programming #code