Kubernetes + Ansible Project

Prerequisites:
Ansible installed on your system
An Ubuntu server for Kubernetes setup

Deployment Steps:

1️⃣ Install Kubernetes using Ansible:
    ansible-playbook -i hosts ansible/install_docker.yml
    ansible-playbook -i hosts ansible/install_k8s.yml
    ansible-playbook -i hosts ansible/setup_cluster.yml

2️⃣ Build the Docker Image:
Navigate to the application directory and build the Docker image:
    cd app
    docker build -t my-web-app .

3️⃣ Deploy the Application on Kubernetes:
Apply the Kubernetes configuration files to deploy the application:
    kubectl apply -f k8s/deployment.yml
    kubectl apply -f k8s/service.yml

4️⃣ Verify Deployment:
Check the status of the running pods and services:
    kubectl get pods
    kubectl get services