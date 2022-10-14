# Docker Guide

## How to use an existing image from dockerhub : docker/getting-started

1 . docker pull docker/getting-started

2 . docker run -d -p 80:80 docker/getting-started

3 . docker ps

4 . Open browser : 127.0.0.1:80 and enter . It will show as http://127.0.0.1/tutorial/ which runs on container


# Create , Push and Pull


## 1 . Create an image :

1 . Write your webapp and programs . Create a Dockerfile

2 . docker build -t welcome-app .

3 . docker images


## 2 . Run an image :

1 . docker run -d -p 5000:5000 welcome-app

2 . Open browser : http://127.0.0.1:5000/

* remove commands

docker ps

docker rmi -f welcome-app

docker rmi ece0ce4ea5d4

* stop commands

docker stop ed9c49245123

docker ps

docker images


## 3 . Push to Dockerhub :

1 . docker build -t jateendra/welcomeapp .

2 . docker images

3 . docker ps

4 . docker push jateendra/welcomeapp:latest

     ```
     If error use : docker login
     give your cridentials
     ```
     
## 4 . Pull from Dockerhub :    

1 . docker pull jateendra/welcomeapp

2 . docker run -d -p 5000:5000 jateendra/welcomeapp

3 . docker ps

4 . Open browser : http://127.0.0.1:5000/

# Docker playground :

1 . https://labs.play-with-docker.com/
