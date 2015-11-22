# Generic PHP container

Generic PHP container built on CentOs 7.

Note:

This repo just serves as a base image for building PHP based containers. You can extend this by using the existing image (the result of this Docker file repo) at https://registry.hub.docker.com/u/lysender/php by Docker Hub. 

This image provides no entry scripts that can be daemonized, instead, it just prints a text and exists. 

## Requirements

You must have at least Docker 1.6.2 where this Dockerfile is tested. It is also nice to have a fast internet connection or best if you do this on a VPS or some cloud hosting account.

## Installation

For testing purposes, like a hello workd application (in our case, a php -i output), we can build the image this way.

Note: I prefer to create images and containers as a regular user. You may choose to run it as root.

    # Clone this repo
    git clone git@github.com:lysender/docker-php.git
    cd docker-php
    
    # Build image, you can use any tag name
    docker build --rm -t lysender/php .
    
    # Create and run a container, then delete it
    docker run --rm lysender/php

The first part (building the image) will take some time to complete. Fast connection helps.

