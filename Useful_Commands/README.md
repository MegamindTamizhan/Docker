# Creating a Docker Image from an Running Container

    $ docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
     
     Eg: docker commit -m "apache + php" myubuntu megamindtamizhan\myubuntu:latest

# How to copy Docker images from one host to another without using a repository

    $ docker save [OPTIONS] IMAGE [IMAGE...]
    
     Eg: docker save myubuntu > myubuntubak.tar

        