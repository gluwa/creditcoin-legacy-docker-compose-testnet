#1 Install docker and docker-compose

#2 Fill in Client/clientConfig.json, optionally Validator/gatewayConfig.json if you choose to run a local gateway

#3 Open up Validator/creditcoin-default.yaml or Validator/creditcoin-with-gateway.yaml, replace [insert.your.ip] with your public ip.

#4 docker-compose -f creditcoin-default.yaml up 
Use creditcoin-with-gateway.yaml if you want to run a local gateway
Add "-d" without quotes if you need to run it in the background

FOR WINDOWS: make sure you allow docker access to your harddrive in Settings => Shared Drives

Using the client

#1 Navigate to the /Client folder and start the client container with: 
docker-compose -f creditcoin-client.yaml up -d

#2 Log into the container with:
docker exec -it creditcoin-client bash

#3 use ./ccclient to run your creditcoin commands, for example:
./ccclient 

#4 use ctrl+pq to log out of the container

#5 shut down the container with:
docker-compose -f creditcoin-client.yaml down