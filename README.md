
# Networking CA1 – Automated Web Application Deployment

## Overview

This project automates the deployment of a web application using Terraform for infrastructure provisioning and GitHub Actions for continuous integration and deployment.

## Project Structure

- `.github/workflows/` – Contains GitHub Actions workflow files for automation.
- `webapp/` – Directory for the web application's source code.
- `main.tf` – Terraform configuration file defining the infrastructure resources.
- `backend.tf` – Terraform backend configuration for state management.

## Automation Flow

1. **Version Control with GitHub**
   - Code is pushed to the GitHub repository, triggering workflows.

2. **Infrastructure Provisioning with Terraform**
   - `main.tf` defines the necessary infrastructure (e.g., servers, networking).
   - `backend.tf` configures the backend for storing Terraform state securely.
   - Terraform commands (`init`, `plan`, `apply`) are used to provision resources.

3. **CI/CD with GitHub Actions**
   - Workflows in `.github/workflows/` automate testing and deployment processes.
   - On code push, the workflow:
     - Checks out the repository code.
     - Sets up the necessary environment.
     - Runs tests on the web application.
     - Deploys the application to the provisioned infrastructure.

## Notes

- Ensure that all necessary secrets and environment variables are set in the GitHub repository settings for the workflows to function correctly.
- Modify the Terraform and workflow files as needed to suit specific infrastructure and deployment requirements.
