Lab 13 – Kubernetes Deployment
INET 4031 – Introduction to Systems
This lab extends the Docker-based application developed in Lab 12 by migrating it into a Kubernetes environment using k3s. Instead of relying on Docker Compose to manage containers, Kubernetes is used to deploy and orchestrate the application through declarative configuration files.

Project Overview
The project is a ticket management system that allows users to view and submit IT support requests. It is built using a three-tier architecture consisting of:
a frontend interface for user interaction
a backend API that handles application logic and requests
a database that stores ticket information
In this lab, each component is deployed within a Kubernetes cluster, improving scalability, resilience, and overall system management.
Key Changes from Lab 12
This lab transitions the application from Docker Compose to Kubernetes. Rather than manually managing containers, Kubernetes handles deployment through resources such as Deployments, Services, and PersistentVolumeClaims.
Configuration values that were previously stored in a .env file are now managed using Kubernetes Secrets.

This shift introduces several improvements, including:

automated container orchestration
self-healing capabilities for failed pods
persistent storage for database data
clearer separation of application components
Deployment
All components are deployed using Kubernetes manifest files located in the k8s directory. These manifests define how each service runs within the cluster, including the database, backend API, and frontend web server.
Accessing the Application
After all pods are successfully running, the application can be accessed through a web browser using the NodePort assigned by Kubernetes. The web interface allows users to view and manage support tickets.
Database Initialization
The database is initialized using a provided SQL script that creates the required schema and inserts sample ticket data. This ensures the application has preloaded data for testing and verification purposes.
Verification
The system is considered correctly deployed when:
all pods (web, app, and database) are running
the frontend loads successfully in a browser
the API health endpoint confirms database connectivity
ticket data can be retrieved through the API
A provided validation script can be used to automatically verify that all components are functioning as expected.
Self-Healing
A key feature demonstrated in this lab is Kubernetes self-healing. If a pod is deleted or fails, Kubernetes automatically recreates it to match the desired state defined in the deployment configuration. This ensures the application remains available without manual recovery steps.
Summary
This lab demonstrates how a multi-component application can be deployed and managed using Kubernetes. It highlights core benefits of orchestration systems such as reliability, scalability, and automated recovery. Moving from Docker Compose to Kubernetes provides a practical introduction to modern cloud-native deployment practices and DevOps workflows.
