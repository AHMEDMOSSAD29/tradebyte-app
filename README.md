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


