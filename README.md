# docker-test
This simple project to for docker exercises. 

## How to build docker image from Dockerfile

```
docker build -t flask-test-app .
```

## Run container in detached mode with assigned name

```
docker run -itd  -p 5000:5000 --name flaskapp  flask-test-app
```

## Inspect container

```declarative
docker container inspect flaskapp
```

## See container logs

```declarative
docker logs flaskapp
```
## Enter inside container 

```declarative
docker container exec -it flaskapp sh
```

## Stop and remove all the containers

```declarative
docker container rm $(docker ps -aq) --force
```
## Remove image

```declarative
docker image rmi  <image_name>
```
## Build image and run container from docker compose

```declarative
docker-compose up -d
```
## Add user to app 

```declarative
curl -X POST http://localhost:5000/users \
-H "Content-Type: application/json" \
-d '{"name": "Alice", "email": "alice@example.com"}'

```
