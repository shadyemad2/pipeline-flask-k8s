# 🚀 Flask App Auto-Deploy to Minikube using GitHub Actions

This project demonstrates a complete CI/CD pipeline that automatically builds, pushes, and deploys a Flask app to a local Minikube Kubernetes cluster using GitHub Actions and DockerHub.

<img width="785" height="603" alt="overview" src="https://github.com/user-attachments/assets/af7acdc2-7065-458e-90cc-19af3dac0d87" />


## 📦 Project Structure

```
pipeline-flask-k8s/
├── app.py
├── Dockerfile
├── requirements.txt
├── templates/
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── .github/
│   └── workflows/
│       └── deploy.yml
└── kubeconfig-inline.yaml
```

## 🔧 Tech Stack

- Python + Flask
- Docker & DockerHub
- Kubernetes (Minikube)
- GitHub Actions (self-hosted runner)

## ⚙️ CI/CD Pipeline

1. Push to `master` triggers GitHub Actions
2. The workflow:
   - Builds Docker image
   - Pushes image to DockerHub
   - Connects to Minikube using `kubeconfig` secret
   - Applies `kubectl apply -f k8s/*.yaml`

## 🔐 GitHub Secrets

| Secret Name         | Description                        |
|---------------------|------------------------------------|
| DOCKERHUB_USERNAME  | Your DockerHub username            |
| DOCKERHUB_TOKEN     | DockerHub access token             |
| KUBECONFIG_DATA     | Base64 of your Minikube kubeconfig |

## 📸 Screenshots

> Upload your screenshots to an `images/` folder and update these paths

- ✅ GitHub Actions Success  
 <img width="692" height="212" alt="run-job" src="https://github.com/user-attachments/assets/47b72e9e-5d8e-4e3a-8903-d2474a5a55d0" /> 
 <img width="925" height="758" alt="trigger-github" src="https://github.com/user-attachments/assets/6f3952c5-8aa4-43e2-a1fe-048eeac13b35" />

- ✅ Minikube Pods  
 <img width="659" height="288" alt="kubectl-pods" src="https://github.com/user-attachments/assets/d16e200f-6aa6-455a-b8d2-35a8e1c21b7d" />

- 🌐 Flask App  
 <img width="1860" height="535" alt="flask-app" src="https://github.com/user-attachments/assets/5198ffe9-2285-4ee5-a682-559667748ee2" />


## 🙋‍♂️ Author

**Shady Emad**  
DevOps | Linux | Kubernetes  
[GitHub](https://github.com/shadyemad2)


