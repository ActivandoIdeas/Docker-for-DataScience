# Complete Data Science tools with Docker

This image expose jupyter in port **8888** with password **root**

<div align="center">
  <img src="img/capture.png">
</div>

## Supports

* Anaconda 3 2020
* Jupyter with Support for Autocomplete
* Python
* R
* Scala
* Java
* NodeJs
* Ruby

## Enable autocomplete

 - Click on nbextensions tab
 - Unckeck disable configuration for nbextensions without explicit compatibility
 - Put a check on Hinterland

You can apply more extensions if you need

## How to use?

In Docker run

```bash
docker pull eocode/debian-anaconda-jupyter:202010
```

## Run with this Dockercompose

In your project create docker-compose.yml

```yml
version: "3.8"

services:
  condajupyter:
    build: 
      context: .
      dockerfile: Dockerfile
    container_name: notebooks
    image: eocode/debian-anaconda-jupyter:202010
    tty: true
    ports:
        - 8888:8888
    volumes:
        - ./notebooks:/opt/notebooks
```

Then run

```bash
docker-compose up
```

## Contributtion

Sendme a pull request with your features or improves
Send me a message as @eocode in social networks