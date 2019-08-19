Process To Start the Application.

Pre-Requisites : UBUNTU 18.04/16.04

								--- SETUP ENVIRONMENT ---

1.) Install Git

	$ sudo apt update
	$ sudo apt install git
	$ git --version

2.) Install MAVEN

	$ sudo apt update
	$ sudo apt install maven
	$ maven --version

3.) Install Docker

	$ sudo apt-get update
	$ sudo apt install docker.io
	$ docker --version

4.) Install Docker-compose

	$ sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
	$ sudo chmod +x /usr/local/bin/docker-compose
	$ docker-compose --version



								---- COMMANDS ----
  
1.) Open ubuntu terminal in any folder

	$ git clone https://github.com/mukeshdalavai/wastage-reduction-final.git

2.) Nvigate into wastage-reduction-final folder

	$ mvn clean package -DskipTests
	$ sudo docker-compose up --build
