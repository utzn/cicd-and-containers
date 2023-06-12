# Instructions (written by ChatGPT)

## Project: CI/CD Pipeline for a Flask Web App Deployed on Azure Kubernetes Service (AKS)
This project focuses on developing a simple Flask-based web application, containerizing it using Docker, version controlling it using Git and GitHub, and deploying it on Azure Kubernetes Service (AKS) using a Continuous Integration/Continuous Deployment (CI/CD) pipeline. Here are the steps to guide you:

1. Create a Simple Flask Web App (3-4 hours)
  - Start by creating a simple Flask-based web application. Flask is a lightweight Python web framework that's easy to learn and use. Your application doesn't have to be complex. A simple CRUD (Create, Read, Update, Delete) app that interacts with a SQLite database would be sufficient. There are plenty of tutorials online to guide you through this process.

2. Dockerize the Flask App (3-4 hours)
  - Create a Dockerfile for your Flask application. This Dockerfile will contain the instructions to build a Docker image of your Flask application. The Docker image will include everything your app needs to run, including the Python runtime, Flask framework, and your application code.

3. Push Your App to GitHub (1-2 hours)
  - Create a new repository on GitHub and push your application code to this repository. Make sure to include the Dockerfile and a README with instructions on how to build and run the Docker image.

4. Setup Azure Kubernetes Service (AKS) (4-5 hours)
  - Create an AKS cluster on Azure. This might take some time if you're not familiar with Azure. There are plenty of resources online to guide you. Once your AKS cluster is up and running, you'll need to create a Kubernetes deployment for your Flask app and expose it using a Kubernetes service. The Kubernetes deployment will reference the Docker image of your Flask application.

5. Create a CI/CD Pipeline (8-10 hours)
  - Finally, create a CI/CD pipeline using GitHub Actions or Azure Pipelines (part of Azure DevOps). The pipeline will automate the process of building a new Docker image whenever you push changes to GitHub, pushing the Docker image to a Docker registry (like Docker Hub or Azure Container Registry), and updating the Kubernetes deployment on AKS to use the new Docker image.
  - This CI/CD pipeline ensures that every change you make to your application is automatically deployed to your AKS cluster. It enables you to practice the principle of "continuous deployment," where every change that passes the automated tests is automatically deployed to production.

6. Learning and Research (4 hours)
  - This time is scattered throughout the project and is spent learning concepts, troubleshooting issues, and understanding the tools and technologies you're working with.
  - This project will help you understand and gain practical experience with several important concepts and technologies, including Flask, Docker, Kubernetes, CI/CD, GitHub, and Azure. It's a comprehensive and practical project to learn about CI/CD and containers.

7. Adding Automated Testing (3-4 hours)
  - Before integrating and deploying your changes, it's crucial to ensure your application is working as expected.
  - Write unit tests for your application using a Python testing library like pytest or unittest. This helps verify the functionality of individual pieces of your app.
  - Incorporate these tests into your CI/CD pipeline. On each git push, the pipeline should run these tests automatically. If the tests fail, the pipeline should stop, helping you catch issues before they reach the production environment.

8. Container Scanning and Security Checks (2-3 hours)
  - Security is a critical aspect of any application.
  - Add a step in your pipeline to scan your Docker images for known vulnerabilities. Tools like Trivy can be used for this purpose.
  - Use Azure Security Center for additional security and threat detection capabilities. It takes some time to understand these features and set up policies, but it contributes to the overall robustness of your deployment.

9. Advanced Kubernetes Features (2-3 hours)
  - Take advantage of more advanced Kubernetes features to enhance your application.
  - Implement Kubernetes liveness and readiness probes in your deployment. These probes help Kubernetes make intelligent decisions about when to restart your app's containers and when to send traffic to them.
  - Set up a Kubernetes Horizontal Pod Autoscaler. This automatically scales the number of pods in your deployment based on CPU utilization or other select metrics.

10. Incorporating a Managed Database Service (2-3 hours)
  - Rather than using SQLite, integrate your application with a managed database service in Azure like Azure PostgreSQL or Azure Cosmos DB. This offers experience with cloud databases, connection security, and potentially database migrations.

11. Observability (3-4 hours)
  - Implement observability tools into your application.
  - Incorporate application logging using a service like Azure Monitor. Modify your Flask app to output useful log information, then configure Azure Monitor to collect and analyze this data.
  - Set up application performance monitoring using Azure Application Insights. This involves adding the Application Insights SDK to your Flask app.
