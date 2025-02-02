# Script Setup Guide

This README outlines the activities that are automated by the setup script, which configures environment variables, creates GitLab projects, sets up runners, clones repositories, and configures integration with Azure DevOps.

## Activities Performed by the Script

### At First Run

1. **Create Library ENV**  
   The script creates a centralized library environment that holds configuration settings required for the project. This allows for easy management of variables and settings across different project components.

2. **Create VAR az-pat**  
   The script creates a variable `az-pat` to store the Azure Personal Access Token. This token is essential for authenticating against Azure services.

3. **Create VAR az-org-name**  
   The script sets the variable `az-org-name` to define the Azure organization name, which is used for identifying your organization within Azure.

4. **Create VAR az-org-url**  
   The script sets the variable `az-org-url` to define the URL of your Azure organization, which is required to interact with the Azure API.

5. **Create VAR gitlab-root-group**  
   The script creates the variable `gitlab-root-group` to store the name of the GitLab root group. This is used for organizing projects and other GitLab resources.

6. **Create VAR gitlab-pat**  
   The script creates a variable `gitlab-pat` to store the GitLab Personal Access Token, which is needed to authenticate against the GitLab API and perform actions on GitLab resources.

7. **Create GitLab Project Builder (under gitlab-root-group)**  
   The script creates a GitLab project named **Project Builder** under the specified GitLab root group. This project serves as the template or starting point for building the application.

8. **Clone Repo https://github.com/automiter/Builder into GitLab Project Builder**  
   The script clones the **Builder** repository from GitHub into the newly created GitLab **Project Builder**.

9. **Create GitLab Project Runner (under gitlab-root-group)**  
   The script creates a GitLab project named **Project Runner** under the GitLab root group. This runner will be used for continuous integration and deployment (CI/CD) tasks associated with the project.

10. **Clone Repo https://github.com/automiter/Runner into GitLab Project Runner**  
    The script clones the **Runner** repository from GitHub into the newly created GitLab **Project Runner**.

11. **Create GitLab Pipeline Trigger Token**  
    The script creates a trigger token for the GitLab pipeline. This token will be used to trigger GitLab CI/CD pipelines.

12. **Create Azure DevOps Self-Hosted Agent**  
    The script automates the creation of a self-hosted agent in Azure DevOps, allowing the system to interact with Azure DevOps environments for pipeline execution.

---

### At Other Runs

1. **Create Azure DevOps Project**  
   The script creates a new Azure DevOps project as needed for the CI/CD pipeline setup.

2. **Add Service-Hook Webhook with the GitLab Trigger Token URL (Job State Change: Waiting)**  
   The script configures a service hook in Azure DevOps to listen for job state changes, specifically when the job is in a "waiting" state. The webhook uses the GitLab trigger token URL to trigger the corresponding action in GitLab.

---

## Requirements

Before running the script, ensure you have the following:

- **Azure Personal Access Token (az-pat)**
- **Azure Organization Name (az-org-name)**
- **Azure Organization URL (az-org-url)**
- **GitLab Personal Access Token (gitlab-pat)**
- **GitLab Root Group Name (gitlab-root-group)**

---

## Notes
- The script automates project creation, environment configuration, repository cloning, and integration with both GitLab and Azure DevOps, simplifying the setup process.
- Ensure that you have the necessary permissions to create projects, manage access tokens, and configure webhooks in both Azure DevOps and GitLab.
- Modify the script as needed to meet specific configurations or add additional settings for your environment.

---
