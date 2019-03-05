# docker
Docker containers for ALA or Canadensys

## Example
```
$ git clone https://github.com/Canadensys/docker.git ; cd docker/grails-java7
$ docker build -t grails:2.3.11 --build-arg grails_version=2.3.11 .
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.3.11 clean-all
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.3.11 war
```
Or
```
$ git clone https://github.com/Canadensys/docker.git ; cd docker/grails-java8
$ docker build -t grails:2.5.6 --build-arg grails_version=2.5.6 .
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 clean-all
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 refresh-dependencies --non-interactive
$ docker run --rm -v /home/path_to_your_ala_app/:/app:rw --name grails grails:2.5.6 prod maven-install --non-interactive war
```

