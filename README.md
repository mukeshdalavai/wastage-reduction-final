					------Working Protocols-----
-> Every Noon (12-4) --> Restaurants update their respective food availability.
		  --> Charities may update their food requirement if incase there are any modifications.
		  --> Delivery Boys will update their Availability status and Live Location.
		  
 -> An automatic API call is made at 4.0PM and the ROUTING PROTOCOL is initiated which maps Restaurants, Charities and DeliveryBoys, Followed by Optimal Route Allocation to Delivery Boys (Restaurants to pick-up and Charity to deliver).
 
 -> After Succesful Delivery of food, Charities has the luxury to Rate the food received to ensure donation of quality food.
 
-> Upon completion of all transactions, another API Call is made which RESET'S the entire application making it ready for the next Noon.

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
.


						---- COMMANDS ----
  
1.) Open ubuntu terminal in any folder

	$ git clone https://github.com/mukeshdalavai/wastage-reduction-final.git

2.) Nvigate into wastage-reduction-final folder

	$ mvn clean package -DskipTests
	$ sudo docker-compose up --build
