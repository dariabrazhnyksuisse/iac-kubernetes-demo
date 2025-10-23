# 🚀 IaC Kubernetes Demo

This repository demonstrates a full Infrastructure-as-Code (IaC) workflow for deploying a containerized Spring Boot REST API to Kubernetes, monitored with Prometheus & Grafana, and managed through Argo CD GitOps automation.

---

## 📁 Project Structure

| File               | Description                                                                                                                          |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `deployment.yaml`  | Defines the Kubernetes Deployment for the `hello-world` REST API                                                                     |
| `service.yaml`     | Exposes the application using a NodePort service                                                                                     |
| `playbook-k8s.yml` | Ansible playbook to automate namespace creation, manifest application, and optional installation of Prometheus, Grafana, and Argo CD |

---

## ⚙️ Tools & Technologies

- **Docker** – containerized REST API (`dariabrazhnyk/hello-world-rest-api`)
- **Kubernetes** – container orchestration
- **Ansible** – Infrastructure-as-Code automation
- **Grafana & Prometheus** – real-time cluster monitoring
- **Argo CD** – GitOps-based CI/CD visualization
- **VS Code on WSL (Ubuntu)** – development environment

---

## 🧠 Demo Flow

1. Deploy manifests using Ansible:
   ```bash
   ansible-playbook -i localhost, -e ansible_python_interpreter=$VIRTUAL_ENV/bin/python playbook-k8s.yml
   ```
