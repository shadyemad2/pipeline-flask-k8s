# 🚀 Flask App Auto-Deploy to Minikube using GitHub Actions

This project demonstrates a complete CI/CD pipeline that automatically builds, pushes, and deploys a Flask app to a local Minikube Kubernetes cluster using GitHub Actions and DockerHub.

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
  ![CI Success](images/github-actions-success.png)

- ✅ Minikube Pods  
  ![Pods](images/kubectl-get-pods.png)

- 🌐 Flask App  
  ![App](images/flask-app-running.png)



## 🙋‍♂️ Author

**Shady Emad**  
DevOps | Linux | Kubernetes  
[GitHub](https://github.com/shadyemad2)


