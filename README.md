# AWS Portfolio - Docker & Kubernetes

A simple portfolio website containerized with Docker and deployed using Kubernetes.

# Architecture

                +------------------+
                |      User        |
                |     Browser      |
                +--------+---------+
                         |
                         v
                +------------------+
                | Kubernetes       |
                |    Service       |
                +--------+---------+
                         |
                         v
                +------------------+
                | Kubernetes       |
                |      Pod         |
                +--------+---------+
                         |
                         v
                +------------------+
                |      Nginx       |
                |  Web Server      |
                +--------+---------+
                         |
                         v
                +------------------+
                | Portfolio Site   |
                |    index.html    |
                +------------------+

# Project Structure
.
├── .github/
│ └── workflows/
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── index.html
└── README.md

# Technologies Used
HTML
Docker
Nginx
Kubernetes
GitHub
GitHub Actions
Containerization

The portfolio website is packaged into a Docker image using Nginx as the web server.

# Build Image
docker build -t aws-portfolio .
# Run Container

docker run -d -p 8080:80 aws-portfolio

Access: http://localhost:8080

# Kubernetes Deployment

Deploy the application:

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Verify resources:
kubectl get deployments
kubectl get pods
kubectl get services

# Skills Demonstrated
Containerization with Docker
Web hosting with Nginx
Kubernetes Deployments
Kubernetes Services
Source Control with Git
Infrastructure Fundamentals
Cloud-Native Concepts

# Future Improvements
Terraform Infrastructure as Code
AWS EC2 Deployment
AWS EKS Integration
CI/CD Pipeline Enhancements
Monitoring with Prometheus and Grafana
