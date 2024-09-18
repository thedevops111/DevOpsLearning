# 🚀 DevOps Journey: Step-by-Step Guide
Welcome to the DevOps journey! This guide provides steps for setting up version control, creating a CI pipeline, and learning essential DevOps tools and practices.

## Table of Contents
1. What is DevOps?
2. Prerequisites
3. Step-by-Step: Creating a GitHub Repository
4. Creating a CI Workflow
5. Next Steps

## What is DevOps?
**DevOps** combines software development and IT operations to enable continuous delivery and high-quality releases in shorter timeframes.

## Prerequisites
Before starting, ensure you are familiar with:

* **Git**: For version control.
* **GitHub**: For hosting repositories.
* **Basic Programming Knowledge**: Familiarity with languages like Python, Java, or Node.js will help.
* **Basic Command-Line Interface (CLI) Knowledge**: Be comfortable with terminal commands.

## Step-by-Step: Creating a GitHub Repository
### 1. Sign Up for GitHub
1. Go to [GitHub](https://github.com/) and create an account.

2. After registering, you can create a **New repository**.
   
### 2. Create a New Repository
To create your first repository:

1. Click on the New button in the top right.
2. Name your repository (e.g., my-devops-journey).
3. Add a short description (optional).
4. Choose the visibility (Public or Private).
5. Check the box to initialize with a README.md file.
6. Click Create repository.
   
### 3. Clone Your Repository
Once the repository is created:

#### 1. Open your terminal.
#### 2. Clone the repository:
bash
Copy code
git clone [https://github.com/](https://github.com/thedevops111/DevOpsLearning.git)
#### 3. Navigate into your project directory:
bash
Copy code
cd my-devops-journey

### 4. Commit and Push Changes
To update the repository with your code:

#### 1. Stage your changes:
bash
Copy code
git add .
#### 2. Commit the changes:
bash
Copy code
git commit -m "Initial commit"
#### 3. Push the changes to the GitHub repository:
bash
Copy code
git push origin main

## Creating a CI Workflow
Use GitHub Actions for automating the CI pipeline. Here’s a basic guide:

### 1. Add a Workflow
In your repository, click on the **Actions** tab.
Choose **Set up a workflow yourself**.

### 2. Define the Workflow
Add the following code to .github/workflows/ci.yml:


```
name: CI Pipeline

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```
        
### 3. Monitor Workflow
Go to the Actions tab to view the status of your CI pipeline.
A green checkmark indicates success, while a red cross shows a failure.

## Next Steps
* **Explore Continuous Deployment (CD)**: Automate your deployment process.
* **Learn Infrastructure as Code (IaC)**: Use tools like Terraform or Ansible to manage infrastructure.
* **Containerization**: Start using Docker and Kubernetes.
