## Dockerfile development configuration

For Vanilla Latest PHP using Ubuntu 20.04 as base image

Stack

* Nginx
* PHP-FPM 
* Latest PHP version 8.0.3


Loaded PHP Extensions

* Mysql
* Intl
* Mbstring
* Zip
* Xml
* Sqlite3


## Compile the docker file

```
docker build -t vanillaphplatest_20.04-image -f Dockerfile.dev .
```

## Create instance of the container

```
docker run -p 8080:80 -dit --name conainer_name-web --mount type=bind,source="$(pwd)",target=/var/www/html vanillaphplatest_20.04-image
```


## Manage the container

```
docker exec -it conainer_name-web bash
```


## Usage

1. Build the dockerfile configuration and create a container for it.

2. Now that you have your container setup, you can access it via

```
docker exec -it <project-name> bash	
```

3. You should be able to load your web-application from your browser with the port you incidated above. Example: http://localhost:8080


