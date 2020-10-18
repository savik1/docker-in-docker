Docerfile для образа "buid_docker_image"

FROM maven:3.5.4-alpine \
RUN apk add --update docker \
WORKDIR /home/user 
