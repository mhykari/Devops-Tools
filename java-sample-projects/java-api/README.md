# java-api-test
This Repository contains a simple java api for test on docker and kubernetes. this project needs maven to compile the project and the dockerfile has to be build so finaly we have a docker image to use on docker or k8s.  <br />
  <br />
install maven:  <br />
sudo apt install maven -y  <br />
mvn -version  <br />
  <br />
where the pom.xml file is:  <br />
mvn clean package  <br />
  <br />
where th dockerfiles is:  <br />
docker build -t java-api:1.0 .  <br />
  <br />
to run by java:  <br />
java -jar target/java-api-1.0-SNAPSHOT.jar  <br />
  <br />
run on docker:  <br />
docker run -d --name java-api-test -p 8080:80 java-api:1.0  <br />
