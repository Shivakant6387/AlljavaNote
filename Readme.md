	#### Access the end points
POST: http://localhost:8080/myAccount
use payload :
{"customerId":1}

#H2 console

http://localhost:8080/h2-console
#### JDBC URL
jdbc:h2:mem:testdb
#####
https://github.com/prpramod/accounts/commit/e212f1d5de31c796912ce7dcfe585a465b63ea79

#### Creating ,building the docker image 
create Dockerfile (included in this repo)
docker build . -t pramodpra/accounts
docker run -p 8080:8080 pramodpra/accounts
docker run -d -p 8080:8080 pramodpra/accounts
docker push docker.io/pramodpra/accounts

docker images
docker image inspect <image-id>
docker container inspect <container-id>
docker logs <container id>
docker logs -f <container id>
docker stop <container id>
docker ps -a
docker start <container id1> <container id2>
#####Dont take any requests for this container
docker container pause <container id> 

docker container unpause <container id> 
##### docker kill <container-id> vs docker stop <container-id>

docker stats 

docker rm <container-id>
docker rmi <image-id>
docker container prune

##### Springboot commands 
mvn spring-boot:run

##### Build docker images with build pack 
Delete the Dockerfile 
Add the following code snippet 
![img_1.png](img_1.png)
Then run 
mvn spring-boot:build-image
docker images to verify 





