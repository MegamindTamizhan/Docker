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