Lab 13 – Kubernetes Deployment
INET 4031 - Introduction to Systems
- This lab extends the Docker-based application developed in Lab 12 by migrating it into
  a Kubernetes environment using k3s. Instead of relying on Docker Compose to manage       containers, Kubernetes is used to deploy and orchestrate the application through         declarative configuration files.
-----------------------------------------------------------------------------------------
Project Overview
This lab extends the Docker-based application developed in Lab 12 by migrating it into a Kubernetes environment using k3s. Instead of relying on Docker Compose to manage containers, Kubernetes is used to deploy and orchestrate the application through declarative configuration files.
- a frontend interface for user interaction
- a backend API that handles application logic and requests
- a database that stores ticket information
The project is a ticket management system that allows users to view and submit IT support requests. It is built using a three-tier architecture consisting of:
-----------------------------------------------------------------------------------------
