Create a docker file for tomcat which will add sample.war into webapp folder. Here tomcat used is bundled with alphine OS
Mention the running script in command along with the port
Then create the image.

http://192.168.99.100:80/sample/   ----> To execute the war

Commands Used :
$ docker search tomcat                         ---------->  search for tomcat images
$ docker build -t vibzdocker/samtomcatalphine .
$ docker image ls -a
$ docker container run -d -p 80:8080 --name tomcont vibzdocker/samtomcatalphine
$ docker container ls -a