# CA2 - part 3 & 4
## branch name: master
### DOCKER
***
* Create a *docker network*:
docker network create mysql

* Provide a command that will run a mysql:latest docker image with the name of db with a root password=my-secret-password:
* docker run --network mysql -v $(pwd)/db/datadir:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=my-password --name mysql -d mysql

* Provide a command that will run the docker image phpmyadmin/phpmyadmin on the network previously created mapping a port of your choice to port 80 of the container:
docker run --network mysql -p 83.212.126.249:8083:80 -e PMA_HOST=mysql -d phpmyadmin/phpmyadmin