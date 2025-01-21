# Automiter Package Setup Guide

This guide outlines the necessary steps to set up your Azure DevOps organization, GitLab groups, and repository for importing the "automiter" package.

## Prerequisites

- An **Azure DevOps** organization.
- A **GitLab** account with appropriate permissions to create groups and repositories.
- Access to the **Suite** repository from Automiter on GitHub: [Automiter Suite GitHub Repository](https://github.com/automiter/Suite.git).

## Steps for Setup

### 1. Create Azure DevOps Organization

To begin using Automiter, you'll first need an Azure DevOps organization. If you don't already have one, follow these steps:

- Go to [Azure DevOps](https://dev.azure.com/).
- Sign in with your Microsoft account.
- Create a new organization by clicking **Create organization**.
- Choose a name for your organization and follow the prompts.

### 2. Create a Project in Azure DevOps

Once your organization is set up, you need to create a project to host your pipelines and artifacts:

- Inside your Azure DevOps organization, navigate to the **Projects** section.
- Click **New Project**.
- Name your project "Automiter".
- Set the visibility to either **Private** or **Public** depending on your needs.
- Click **Create** to create the project.

### 3. Create GitLab Master Group

Next, you’ll need to create a master group in GitLab:

- Log in to your GitLab account.
- Navigate to the **Groups** section from the sidebar.
- Click **New group**.
- Name the group **Master**.
- Set the group visibility to your preferred setting (Public or Private).
- Click **Create group**.

### 4. Create Subgroup Named "Automiter"

Within the **Master** group in GitLab, create a new subgroup named "Automiter":

- Inside the **Master** group, click on **New subgroup**.
- Name the subgroup **Automiter**.
- Set the visibility to your preferred setting.
- Click **Create subgroup**.

### 5. Create Repository Named "Suite" in GitLab

Now, create the repository for importing the code from the Automiter GitHub repository:

- Navigate to the **Automiter** subgroup within GitLab.
- Click on **New project**.
- Name the project **Suite**.
- Select **Import project**.
- Under **Import project from**, choose **GitHub**.
- In the **GitHub repository URL** field, enter: `https://github.com/automiter/Suite.git`.
- Follow the prompts to import the repository from GitHub into GitLab.

### 6. Import Automiter Code into GitLab Repository

Once you have completed the above steps, the **Suite** repository from Automiter will be imported into your GitLab **Automiter** subgroup.

You can now configure your Azure DevOps pipelines to interact with the **Suite** repository in GitLab for your development process.

## Conclusion

You have now completed the setup to import the **Automiter** package. You can start using it by following the next steps in the Automiter documentation to integrate it with your workflow.

If you have any questions or run into issues, feel free to reach out to the Automiter support team or consult the official documentation.

## Contact

For further assistance or to report any issues, please contact us at [Automiter Support](mailto:support@automiter.com).
