# Healthcare DevOps Project: Automated CI/CD Pipeline

This project demonstrates a fully automated DevOps pipeline for a healthcare application, leveraging industry-standard tools to ensure reliable, secure, and rapid delivery of code across development, staging, and production environments.

---

## Tools Used

- **Git**: Version control for tracking code changes.
- **Jenkins**: Continuous Integration/Continuous Deployment (CI/CD) automation.
- **Docker**: Containerization of applications for consistency across environments.
- **Ansible**: Configuration management and environment provisioning.
- **Selenium**: Automated testing of deployed web applications.
- **Terraform**: Infrastructure provisioning as code.
- **Kubernetes**: Orchestration and management of containerized applications.
- **Prometheus**: Monitoring of application and infrastructure health.
- **Grafana**: Visualization of monitoring metrics.

---

## Business Challenge/Requirement

The goal is to implement a robust DevOps pipeline that:

- Automatically builds, tests, and deploys code triggered by a push to the Git master branch.
- Provisions and configures environments on demand.
- Ensures code quality through automated testing before production deployment.
- Monitors application and infrastructure health in real time.

---

## Workflow Overview

1. **Code Commit & Trigger**
    - Developers push code to the Git master branch.
    - Jenkins is automatically triggered by the push event.

2. **CI/CD Pipeline Execution**
    - **Checkout & Build**: Jenkins checks out the latest code, compiles, and packages it.
    - **Testing**: Automated tests are run (unit/integration) using Jenkins and Selenium.
    - **Containerization**: The application is built into a Docker image.
    - **Artifact Storage**: Docker images are pushed to a container registry.

3. **Infrastructure Provisioning**
    - **Terraform** provisions a new test Kubernetes cluster with at least two nodes.
    - **Ansible** configures the cluster with all required dependencies.

4. **Deployment to Test Environment**
    - Jenkins deploys the Dockerized application to the test Kubernetes cluster.
    - Health checks ensure the cluster and application are running as expected.

5. **Automated Testing**
    - Selenium executes end-to-end tests on the deployed application.
    - Test results determine pipeline progression.

6. **Promotion to Production**
    - If all tests pass, Jenkins deploys the application to the production Kubernetes cluster using the same automated process.

7. **Monitoring & Visualization**
    - **Prometheus** continuously monitors both clusters for health and performance metrics.
    - **Grafana** provides real-time dashboards for visualization of metrics and alerts.

---

## Key Features

- **One-Click Deployment**: End-to-end automation from code push to production deployment.
- **Environment Consistency**: Docker and Kubernetes ensure identical environments across dev, test, and prod.
- **Automated Quality Gates**: Tests and health checks prevent bad code from reaching production.
- **Scalable & Observable**: Infrastructure scales as needed and is monitored in real time.

> *By implementing this Jenkins CI/CD Pipeline with Ansible, Docker, and GitHub, teams can achieve faster release cycles, reduced human errors, improved collaboration between development and operations teams, and ultimately deliver high-quality software with greater efficiency and reliability.*
