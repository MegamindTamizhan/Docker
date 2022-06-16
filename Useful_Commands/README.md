# Creating a Docker Image from an Running Container

    $ docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
     
      Eg: docker commit -m "apache + php" myubuntu megamindtamizhan\myubuntu:latest

# Docker Image Save: Save one or more images to a tar archive

    $ docker save [OPTIONS] IMAGE [IMAGE...]
    
      Eg: docker save myubuntu > myubuntubak.tar

      # Archived Image Move to Another Host

        $ scp myubuntubak.tar root@192.168.5.170:/home/megamind

# Load an image or repository from a tar archive (even if compressed with gzip, bzip2, or xz) from a file or STDIN. It restores both images and tags

    $ docker load [OPTIONS]

      Eg: docker load < myubuntubak.tar
        docker load -i myubuntubak.tar

# Fetch the logs of a container

    $ docker logs Container Name or ID

      Eg: docker logs portainer

# Docker Container Registry Login

    $ docker login
    $ Username:
    $ Password:

# Other Container Registry Login

    $ docker login registry-url
    $ Username:
    $ Password:

# Logout from a Docker Registry

    $ docker logout

# Docker Registry Authentication File

    $ cat ~/.docker/config.json

# OS Container Running Cmd

    $ docker run -dit --name alpineos alpine:latest /bin/sh

    Eg. docker run -dit --name container name image name shell type

# Container OS Login

    $ docker exec -it alpineos /bin/sh

    Eg. docker exec -it container name or ID shell type

# Build an image from a Dockerfile

    $ docker build -t web:v1 .

    Eg. docker build -t image name:tag name .-> Dockerfile path

    $ docker build -t megamindtamizhan/firstnginx_image:v1 .

    Eg. docker build -t dockerhubid/imagename:tagname .-> Dockerfile path

#  Build and Run your App with Compose

    $ docker-compose up -d

    Eg. docker-compose up (-d run in background)

    $ docker-compose up -d app

    Eg. docker-compose up -d app -> container name

# Tag & Push the Docker Image to Docker Hub

    $ docker images
    $ docker tag megamindtamizhan/mynginx_image1:v1 megamindtamizhan/mynginx_image1:v1-release
    $ docker push megamindtamizhan/mynginx_image1:v1-release

      Eg.,
      Replace your docker hub account Id
      docker tag <your-docker-hub-id>/mynginx_image1:v1 <your-docker-hub-id>/mynginx_image1:v1-release
      docker push <your-docker-hub-id>/mynginx_image1:v1-release