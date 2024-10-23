# SWE1-Assignment

Buid Status:  [![Build Status](https://app.travis-ci.com/rohnnie/swe-fall-2024.svg?token=ghd6pxZi8eiJyeoYpQzW&branch=main)](https://app.travis-ci.com/rohnnie/swe-fall-2024)

Coverage:  [![Coverage Status](https://coveralls.io/repos/github/rohnnie/swe-fall-2024/badge.svg?branch=main)](https://coveralls.io/github/rohnnie/swe-fall-2024?branch=main)

# Deploying Django Application on AWS Elastic Beanstalk

This guide provides step-by-step instructions for deploying your Django application on AWS Elastic Beanstalk (EB).

## Prerequisites

- Python 3.11 or higher installed
- AWS CLI and EB CLI installed
- Git installed
- An AWS account

## Steps to Deploy

### 1. Create a Virtual Environment

```zsh
python3.11 -m venv env
```
### 2. Activate the Virtual Environment (Mac/Linux)

```zsh
source ./env/bin/activate
```

### 3. Install Dependencies
Note: Ensure you are installing dependencies using the same Python version that was used to create the virtual environment to avoid errors.
```zsh
pip3.11 install -r requirements.txt
```
### 4. Add the Virtual Environment to .gitignore
```zsh
echo "env/*" >> .gitignore
```

### 5. Initialize Elastic Beanstalk
```zsh
eb init
```
Follow the prompts to configure EB for your project. Choose the region and application platform (Python). Select y for SSH and n for spot fleet instances.

### 6. Create an Elastic Beanstalk Environment
```zsh
eb create
```

### 7. Check Environment Status
```zsh
eb status
```
### 8. Deploy the Application
```zsh
eb deploy
```
### 9. Access Your Application
Once the deployment is complete, you can access your Django application by visiting the URL provided by Elastic Beanstalk.


