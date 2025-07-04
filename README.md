
# Networking CA1 – Automated Container deployment and Administration in the cloud


## Project Structure

- `.github/workflows/` – Contains GitHub Actions workflow files for automation.  
- `ansible/` – Ansible playbook for configuration management and application deployment.  
- `webapp/` – Directory for the web application's source code and Docker container file.  
- `main.tf` – Terraform configuration file defining the infrastructure resources.  
- `backend.tf` – Terraform backend configuration for state management.  

## Automation Flow

1. **Version Control with GitHub**
   - Code is pushed to the GitHub repository, triggering workflows.

2. **Infrastructure Provisioning with Terraform**
   - `main.tf` defines the necessary infrastructure (e.g., servers, networking).
   - `backend.tf` configures the backend for storing Terraform state securely.
   - Terraform commands (`init`, `plan`, `apply`) are used to provision resources.

3. **Configuration Management with Ansible**  
   Ansible playbooks in the `ansible/` directory are used to configure servers and deploy the web application.

4. **Containerization with Docker**  
   The web application is containerized using Docker. The `Dockerfile` specifies the build instructions, and containers are managed as part of the deployment process.

5. **Continuous Integration and Deployment with GitHub Actions**  
   Workflows automate testing, provisioning, and deployment to ensure a seamless CI/CD pipeline.

## Notes

- Ensure that all necessary secrets and environment variables are set in the GitHub repository settings for the workflows to function correctly.
- Modify the Terraform and workflow files as needed to suit specific infrastructure and deployment requirements.
