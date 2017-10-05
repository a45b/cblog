# Cblog (A Rails blog with Cassandra)
---------
## To Run this App
---------------


Install Cassandra in Ubuntu 16.04
---------------------------------

echo "deb http://www.apache.org/dist/cassandra/debian 311x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list

curl https://www.apache.org/dist/cassandra/KEYS | sudo apt-key add -

sudo apt-get update

sudo apt-key adv --keyserver pool.sks-keyservers.net --recv-key A278B781FE4B2BDA

sudo apt-get install cassandra

sudo service cassandra start


Git Clone this Project
----------------------

cd cblog

rake cequel:keyspace:create

rake cequel:migrate

rails s

Go to http://localhost:3000

