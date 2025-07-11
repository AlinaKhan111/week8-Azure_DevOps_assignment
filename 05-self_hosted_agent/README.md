# Task 5 – Create a Windows Self-Hosted Agent for Azure DevOps
## Objective
### To set up and use a Windows self-hosted agent in Azure DevOps for executing CI/CD pipelines. This helps bypass free-tier limitations (like parallel job restrictions) and gives you full control over the build environment.

## Steps Performed
### Step 1: Download and Extract the Agent
- Navigated to:

```bash
Project Settings → Agent Pools → Default → New agent
```

- Selected Windows as OS and downloaded the agent ZIP.

- Extracted to this local directory:

```bash
C:\Users\MR. RATHORE\OneDrive\Desktop\azure-agent
```

<img width="983" height="519" alt="Image" src="https://github.com/user-attachments/assets/ea08f968-e635-49ee-8aad-c4ecc94c8e6f" />

### Step 2: Configure the Agent
- Opened Command Prompt in the `azure-agent` folder

- Ran:

```bash
config.cmd
```

- Provided:

  - DevOps Org URL

  - PAT token for authentication

  - Agent Pool: Default

  - Agent Name: METORITE



### Step 3: Start the Agent
- Started the agent by running:

```bash
run.cmd
```
<img width="871" height="93" alt="Image" src="https://github.com/user-attachments/assets/19f9ea42-27f4-485f-ae01-a8476e10e750" />



- Agent status appeared as Online under:

```bash
Project Settings → Agent Pools → Default
```
<img width="1858" height="712" alt="Image" src="https://github.com/user-attachments/assets/89959ac2-8770-4662-9742-5a85cf2d65b3" />

### Step 4: Run Pipeline Using Self-Hosted Agent
- Updated the pipeline YAML in BankingApp-CICD project to use the default pool:

```bash
pool:
  name: Default
```
- Ran the full pipeline with build + deployment stages.

- Verified successful execution using the self-hosted agent `METORITE`.



<img width="1919" height="915" alt="Image" src="https://github.com/user-attachments/assets/8a53c8da-a922-4df5-9e38-31129f0a34cf" />

<img width="1501" height="329" alt="Image" src="https://github.com/user-attachments/assets/dc27329e-8382-4812-97ba-6847a9b788ea" />


## Summary
The Windows self-hosted agent setup was successful.

- Agent Name: METORITE
- Project: BankingApp-CICD

## Benefits achieved:

- Removed parallelism restriction from student subscription

- Full control over agent tools and environment

- Verified with a successful pipeline build and deployment

