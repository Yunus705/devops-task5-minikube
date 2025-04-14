# 🚀 DevOps Internship Task 5 - Minikube + Kubernetes App Deployment

This project demonstrates how to set up a local Kubernetes cluster using **Minikube**, deploy an application using **YAML manifests**, scale the deployment, and inspect resources using `kubectl describe`.

---

## 📌 Task Objective

- Create a local Kubernetes cluster using Minikube
- Deploy an NGINX application using YAML
- Expose the app using NodePort service
- Scale the deployment using `kubectl scale`
- Use `kubectl describe` to explore the deployment and pods

---

## 🧰 Tools & Technologies

- Minikube
- Kubectl
- VirtualBox (as driver)
- Kubernetes YAML files

---

## 📁 Project Structure

. ├── nginx-deployment.yaml # Deployment file ├── nginx-service.yaml # Service file ├── screenshots/ # Screenshots folder 
  └── README.md
 
---

## 🛠️ Setup Instructions

Clone this Repository
```bash
git clone https://github.com/Yunus705/devops-task5-minikube.git
```bash
cd IaC-Terraform-Docker

1️⃣ Start Minikube
```bash
minikube start --driver=virtualbox

2️⃣ Create Deployment
```bash
kubectl apply -f nginx-service.yaml

3️⃣ Create Service
```bash
kubectl apply -f nginx-service.yaml

🔎 Verify Resources
View Pods and Services
```bash
kubectl get pods
kubectl get services

Get Minikube IP
```bash
minikube ip
📌 Open browser: http://<minikube-ip>:30001
You should see the NGINX welcome page.

---

🔄 Scale Deployment
```bash
kubectl scale deployment nginx-deployment --replicas=5

✅ Check pods:
```bash
kubectl get pods

---

🧠 Inspect Resources using kubectl describe
Describe Deployment
```bash
kubectl describe deployment nginx-deployment

Describe a Pod
```bashkubectl get pods
kubectl describe pod <pod-name>

---

🧹 Cleanup
```bash
kubectl delete -f nginx-deployment.yaml
kubectl delete -f nginx-service.yaml

---

All screenshots are in the screenshots/ folder.

---

🧾 Author
Yunus Sharif
📧 yunussharif705@705.com

---

📃 Note
This project is part of a hands-on DevOps Internship Task to explore Kubernetes concepts using local Minikube setup.

---




