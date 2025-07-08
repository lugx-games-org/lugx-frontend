# lugx-frontend
Static web frontend for Lugx Gaming. Built with HTML, CSS, and JavaScript, served via NGINX in a container. Deployed on Kubernetes with Ingress as a single public endpoint. Integrates web analytics tracking for ClickHouse.

## Tech Stack
- HTML, CSS, JavaScript
- NGINX
- Docker
- Kubernetes (Minikube & GKE)

## Docker image build and push to docker hub
- docker build -t samathikisalka/lugx-frontend:latest .
- docker push samathikisalka/lugx-frontend:latest .

## Kubernetes Deployment

- kubectl apply -f k8s/frontend-deployment.yaml
- kubectl apply -f k8s/frontend-service.yaml
- kubectl apply -f k8s/lugx-ingress.yaml

Update /etc/hosts with your Minikube IP and domain

<MINIKUBE_IP> lugx.local

##CI/CD Pipeline

This repo uses GitHub Actions to

Build the Docker image
Push to Docker Hub (or GCR)
Deploy to Minikube or GKE using kubectl

  
