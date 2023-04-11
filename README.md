# Docker-Fundamentals-with-Andreas
Docker Fundamentals with Andreas

## Build simple hello world image
docker build -t hello-world .

## build fake user print image
docker build -f dockerfile-user -t hello-user .

## build image for repo and push
docker build -f dockerfile-user -t oso007/hello-user:latest .

docker push oso007/hello-user:latest


## remove image and pull new from repository
docker rmi oso007/hello-user:latest

docker pull oso007/hello-user:latest

## find and remove dangling images
docker images -f dangling=true

docker rmi -f $(docker images -f "dangling=true" -q)
