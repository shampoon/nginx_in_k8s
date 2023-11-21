## Build the image
`docker build -t shampoon/frontend -f ./source/Dockerfile ./source/`

## Run the container
`docker run --rm -p 8000:8000 frontend`

## Install in k8s
```
cd helm
helm upgrade --create-namespace -i --debug -n mynamespace myrelease ./frontend
```