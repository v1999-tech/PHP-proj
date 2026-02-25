This project implements a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline to automate application deployment using Jenkins, Ansible, and Docker.

The pipeline is triggered automatically when code is pushed to the GitHub master branch.

---

## 🏢 Business Requirement

- Automate build and deployment process
- Reduce manual intervention
- Enable faster and reliable releases
- Provision test server automatically
- Deploy containerized PHP application

---

## 🛠️ Tools & Technologies Used

- Git – Version Control
- Jenkins – CI/CD Automation
- Docker – Containerization
- Ansible – Configuration Management
- Puppet Agent – Installed on test server
- Ubuntu Linux – Virtual Machines

---

## 🏗️ Architecture
Developer 
↓ 
GitHub (Master Branch) 
↓ 
Jenkins (Master VM) 
↓
Ansible 
↓ 
Test Server (Slave VM) 
↓ 
Docker Container (PHP Application)


## 🖥️ Infrastructure Setup

### Master VM
- Jenkins Installed
- Ansible Installed
- Git Installed
- SSH Configured

### Slave VM (Test Server)
- Python Installed
- OpenSSH Installed
- Git Installed
- Docker Installed via Ansible

---

## 🔄 CI/CD Pipeline Stages

### Stage 1 – Install Puppet Agent
- Puppet agent installed on slave node

### Stage 2 – Install Docker via Ansible
- Ansible playbook executed from Jenkins
- Docker installed automatically on test server

### Stage 3 – Build & Deploy Application
- Pull latest code from GitHub
- Build Docker image
- Run container on test server

### Post Action (Failure Handling)
- If deployment fails, running container is automatically removed

---

##  Project Structure
project/ 
│ 
├── Dockerfile 
├── Jenkinsfile 
├── ansible/   
└── docker.yml 
├── application source code 
└── README.md
