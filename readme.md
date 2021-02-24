# Database details
![ER Diagram](database-details/er-diagram.png)
![Relational-Schema](database-details/Relational-Schema.png)

# How to run:
These steps were tested on Ubuntu, so if you use other OS, you can find another command to replace
1. Install docker:
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
$ sudo apt update
$ apt-cache policy docker-ce
$ sudo apt install docker-ce
$ sudo systemctl status docker
$ sudo apt install docker-compose

2. After install dockers:
Open terminal in folder downloaded from github
$ sudo docker-compose up
Check if they are running:
$ docker container ls -a
If you Want to down service to re-run scripts to re-create database:
$ sudo docker-compose down -v
$ sudo docker-compose up

Server mysql after running dockers:
link web: http://localhost/
phpmyadmin: http://localhost:8082/
	user root
	pass root

Access database in docker:
	$host = 'mysql';	// is shown in the container ($docker container ls -a)
	$user = getenv('MYSQL_USER'); // save in hidden file 'env'
	$pass = getenv('MYSQL_PASSWORD'); // save in hidden file 'env'
	$conn = mysqli_connect($host, $user, $pass, 'any_database_name');



