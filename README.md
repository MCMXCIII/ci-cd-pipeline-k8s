# CI/CD Pipeline with Kubernetes and GitHub Actions

This repository demonstrates a CI/CD pipeline that automates the building, testing, and deployment of a microservice to a Kubernetes cluster using **GitHub Actions**. It integrates containerization with **Docker**, deployment to **Kubernetes** using `kubectl`, and uses **GitHub Container Registry (GHCR)** for storing container images.

## **Features**

- **GitHub Actions** for CI/CD workflow:
  - Automated build and push of Docker images to GHCR.
  - Deployment of the microservice to a Kubernetes cluster.
- **Kubernetes Deployment**:
  - `deployment.yaml` to manage pods and replicas.
  - `service.yaml` to expose the application via a LoadBalancer.
- **Microservice Application**:
  - Sample Python Flask app running on port `5000`.
- **Helm Chart** (Optional):
  - Helm chart included for templating Kubernetes resources.

---

## **Repository Structure**

```plaintext
ci-cd-pipeline-k8s/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml          # GitHub Actions workflow
│
├── app/
│   ├── Dockerfile             # Dockerfile for building the app container
│   ├── app.py                 # Sample Python Flask app
│   ├── requirements.txt       # Python dependencies for the app
│
├── k8s/
│   ├── deployment.yaml        # Kubernetes Deployment manifest
│   ├── service.yaml           # Kubernetes Service manifest
│
├── helm-chart/
│   ├── templates/             # Helm chart templates
│   ├── Chart.yaml             # Helm chart configuration
│   └── values.yaml            # Default values for Helm chart
│
├── README.md                  # Project documentation
└── LICENSE                    # Project license (optional)

