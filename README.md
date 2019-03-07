# docker
Docker containers for ALA or Canadensys

## Example
```
$ git clone https://github.com/Canadensys/docker.git ; cd docker/grails-java7
$ docker build -t grails:2.3.11 --build-arg grails_version=2.3.11 .
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.3.11 clean-all
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.3.11 war
```
For [ala-collectory](https://github.com/AtlasOfLivingAustralia/ala-collectory) 
```
$ git clone https://github.com/Canadensys/docker.git ; cd docker/grails-java8
$ docker build -t grails:2.5.6 --build-arg grails_version=2.5.6 .
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 grails clean-all
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 grails refresh-dependencies --non-interactive
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 grails prod maven-install --non-interactive war
```
For [ala-hub](https://github.com/AtlasOfLivingAustralia/ala-hub) 
```
$ git clone https://github.com/Canadensys/docker.git ; cd docker/grails-java8
$ docker build -t grails:3.2.11 --build-arg grails_version=3.2.11 .
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:3.2.11 ./gradlew assemble
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:3.2.11 ./gradlew check
```

