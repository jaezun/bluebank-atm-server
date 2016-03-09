## ATM (continuous delivery training application)  
- General presentation : https://drive.google.com/open?id=0B7l9P241qSONRG81a1R2WFhvQWc  
- Hands-on session : http://finaxys.github.io/bluebank-atm-server/#/  
  
N.B. : VMS are needed to schedule this session (https://github.com/Finaxys/vm-formation)  



sudo su


if docker is not started:
sudo service docker start
sudo systemctl start docker



To see the containers:
docker ps

To see the historic of containers:
docker ps -a


Create and run container:


docker run -d -p 9200:9200 -p 9300:9300 -p 5601:5601 -v /volumes/elk:/var/lib/elasticsearch --name="elk-container" sebp/elk:E1L1K4
docker run -d -p 8081:8081 -v /volumes/nexus:/sonatype-work --name="nexus-container" sonatype/nexus:2.11.2-06


Stop container:
docker stop name_of_container or container_id

Delete container: 
docker rm name_of_container or container_id


Change UID:
Search on https://hub.docker.com (prefarable official ver.)
chown 1000:1000 /volumes/jenkins
chown 200:200 /volumes/nexus



To enter the container via bash:
docker exec it name_of_the_container bash



Get user info (incl. UID):
id
ps -ef


