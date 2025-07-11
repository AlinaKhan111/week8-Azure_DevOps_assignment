# Task 2 – Use Pipeline Variables While Configuring Pipelines
## Objective
### To configure and utilize different types of pipeline variables (inline YAML, UI-defined, scoped, and secret) within an Azure DevOps YAML-based CI/CD pipeline. The goal is to ensure reusability, maintainability, and secure handling of sensitive data in the deployment process.

### my_pipeline.yml
<img width="1447" height="889" alt="Image" src="https://github.com/user-attachments/assets/332c7dfb-3f0c-4362-add1-770281203ceb" />


## Steps Performed
### Step 1: Defined Variables in YAML
Used `variables:` block to declare:

- `projectName`, `imageName`, `environment` at the pipeline level

- `buildEnv` inside the `Build` stage for scoped use

### Step 2: Used Variables in Pipeline Steps
Echoed all variables in the Build and Deploy stages using:

```bash
echo "Variable: $(variableName)"
```

### Step 3: Added Variables via Azure DevOps UI
From Pipelines → Edit → Variables Tab, added:

- `buildConfig`: `Release` (regular variable)

- `imageTag`: `v1.0.0` (regular variable)

- `myToken`: `(secret)` (with "Keep this value secret" enabled)

### Step 4: Verified Output in Pipeline Logs
Pipeline logs confirmed that all variables were accessed successfully, and secret variables were masked:

```bash
Deploying project: my-spring-app
Using secret token: ***
```

<img width="597" height="436" alt="Image" src="https://github.com/user-attachments/assets/87e3ff43-f6a9-40cc-8348-4c27e07a0284" />
<img width="1916" height="841" alt="Image" src="https://github.com/user-attachments/assets/b4dee95a-7bb4-41e7-8433-aea58c81a293" />
<img width="1606" height="847" alt="Image" src="https://github.com/user-attachments/assets/dc8bdcdc-1ef3-4b1f-ba96-b02b5e42945a" />


## Summary
This task demonstrates:

- How to use inline and scoped YAML variables

- How to define regular and secret variables in the Azure DevOps UI

- How to access and print those variables in CI/CD steps

- The secure handling of secrets (myToken) with value masking in logs





