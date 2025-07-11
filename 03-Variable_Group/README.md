# Task 3 – Use Variable and Task Groups in Pipelines and Set Scopes for Different Stages
## Objective
### To implement centralized variable management using Variable Groups and apply scoped variables within individual pipeline stages. This promotes reusability, secure secret handling, and stage-specific configuration in Azure DevOps YAML pipelines.

## Steps Performed
### Step 1: Created a Variable Group

- Navigated to Pipelines → Library → + Variable Group

- Created a group named: MyVariableGroup

- Added the following variables:


<img width="1323" height="462" alt="Image" src="https://github.com/user-attachments/assets/071d5ffa-f5a1-4a04-a7f4-d0e204b79768" />





### Step 2: Referenced Variable Group in YAML
In the pipeline YAML, added:

```bash
variables:
- group: MyVariableGroup
```
This allowed access to all variable group values inside the pipeline.

### Step 3: Scoped Variables for Stages
Used different values for buildEnv in each stage using inline stage-specific variables:

```bash
- stage: Build
  variables:
    buildEnv: 'development'

- stage: Deploy
  variables:
    buildEnv: 'production'
```

<img width="1533" height="902" alt="Image" src="https://github.com/user-attachments/assets/0ba06704-e58a-4297-b426-51ee4fefb986" />



### Step 4: Validated Output in Pipeline Logs
- Verified variable values through echo statements printed in logs:


<img width="1917" height="914" alt="Image" src="https://github.com/user-attachments/assets/a6340775-dfda-4cb4-8d49-8f6860734a6e" />


### Build Stage Output logs
<img width="832" height="214" alt="Image" src="https://github.com/user-attachments/assets/82571535-ee13-42a8-9e38-4b256c11dd4d" />


### Deploy Stage Output logs
<img width="732" height="170" alt="Image" src="https://github.com/user-attachments/assets/927f6f39-8506-48ab-b340-0bd532b3d473" />


## Summary
This task demonstrates how to:

- Create and use Variable Groups for centralized variable management

- Apply stage-level scoped variables using YAML

- Use secret variables securely in deployments

- Build a pipeline that adapts variable values by stage (e.g., dev vs prod)



