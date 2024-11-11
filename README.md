# Kubernetes Multi-Container Project

This repository contains a multi-container application setup deployed using Kubernetes. The project demonstrates the deployment of two separate containerized applications within the same Kubernetes cluster, showcasing the orchestration, management, and deployment techniques.

## Project Structure

The repository is organized as follows:


### Container 1 (Kubernetes-container1)

- **Description**: This container serves as [briefly describe its function, e.g., a web server, API backend].
- **Key Components**:
  - `Dockerfile`: Instructions to build the container image.
  - `deployment.yml`: Kubernetes deployment file for managing the pod's lifecycle.
  - `cloudbuild.yaml`: Configuration for cloud-based CI/CD pipelines.
  - `index.js`: Main application logic.
  - `package.json`: Contains project dependencies.

### Container 2 (Kubernetes-container2)

- **Description**: This container serves as [briefly describe its function, e.g., a worker process, data processing module].
- **Key Components**:
  - `Dockerfile`: Instructions to build the container image.
  - `deployment.yml`: Kubernetes deployment file for managing the pod's lifecycle.
  - `cloudbuild.yaml`: Configuration for cloud-based CI/CD pipelines.
  - `index.js`: Main application logic.
  - `package.json`: Contains project dependencies.

## Deployment Instructions

1. **Build Docker Images**:
   Navigate to each container's directory and build the images using:
   ```bash
   docker build -t <your-container1-image-name> ./Kubernetes-container1
   docker build -t <your-container2-image-name> ./kubernetes-container2

2. **Deploy to Kubernetes**:
   Apply the deployment YAML files using:
   ```bash
   kubectl apply -f ./Kubernetes-container1/deployment.yml
   kubectl apply -f ./kubernetes-container2/deployment.yml
   
3. **Verify Deployments**:
   Check the status of your deployments:
   ```bash
   kubectl get pods
   kubectl get deployments

