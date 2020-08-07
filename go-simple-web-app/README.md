# Go Simple Web App

This project is a simple web app with HelloWorld and HealthCheck routes. Purpose of this project is to learn how to deploy a simple Go app on minikube cluster locally.

## Steps

- Create a Go app.
- Create a Docker image.
- Push the Docker image to Dockerhub.
- Create the deployment on kubectl.
- Create a service to expose the deployment.

## Tutorial(s) Followed

- [BogoToBogo](https://www.bogotobogo.com/GoLang/GoLang_Web_Building_Docker_Image_and_Deploy_to_Kubernetes.php)
- [minikube start](https://minikube.sigs.k8s.io/docs/start/)

## Useful Command(s)

- To build the Docker image `docker build -t zulfiqarahmed/go-simple-web-app-img .`
- Run the container `docker run -it -p 3333:3000 --name go-simple-web-app-container zulfiqarahmed/go-simple-web-app-img`
- Push the image to docker hub `docker push zulfiqarahmed/go-simple-web-app-img`
- Create service object `kubectl expose deployment go-simple-web-app --type=NodePort --name=go-simple-web-app-svc --target-port=3000`
- Get minikube's ip address `minikube ip`

## Required Tool(s)

- Docker
- Minikube

## Required Configuration(s)

- NOT SUPPORTED Start minikube with root `sudo minikube start --vm-driver=none`
- NOT SUPPORTED [Docker As minikube driver](https://minikube.sigs.k8s.io/docs/drivers/docker/)
- NOT SUPPORTED [Start minikube cluster with docker driver](https://minikube.sigs.k8s.io/docs/drivers/docker/)

## Link(s) visited

- https://phoenixnap.com/kb/install-minikube-on-ubuntu
- https://minikube.sigs.k8s.io/docs/drivers/docker/
- https://docs.docker.com/engine/install/linux-postinstall/
