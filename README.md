# TradeByte App Helm Chart

This repository contains a Helm chart for deploying a Python application from the [DevOps-Challenge](https://github.com/tradebyte/DevOps-Challenge.git) repository.

## Prerequisites

Before you begin, ensure you have the following installed:
- git
- Docker
- Kubernetes cluster [minikube]
- Helm
- kubectl configured to work with your cluster

## Creating Helm chart Steps

### 1. Clone the Source Repository
First, clone the original application repository:
```bash
git clone https://github.com/tradebyte/DevOps-Challenge.git
```
### 2. Create docker file then Build and Push Docker Image
here is my [docker image](https://hub.docker.com/repository/docker/ahmedmosaad112/tradebyte-app/tags/latest/sha256-5dab5940461efbbae940ab31c08d0eb74d7426608b072957968b4aedcc9436eb)

### 3. Create Kubernetes Manifests
[k8s Manifests](k8s)

### 4. Create Helm Chart
First, create tradebyte:
```bash
helm create tradebyte
```
second, convert k8s manifests files by replacing values in k8s files then put it into vlues.yaml file in the chart and then package tradebyte chart:
```bash
helm package tradebyte
```
third, deploy the application using the Helm chart:
```bash
Helm install tradebyte-app ./tradebyte
```

#### finally if you want to test my chart 
clone this repo 
```bash
git clone https://github.com/AHMEDMOSSAD29/tradebyte-app.git
```
then 
```bash
Helm install tradebyte-app tradebyte/
```
then
```bash
minikube service tradebyte-service
```



