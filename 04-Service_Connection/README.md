# Task 4 – Create a Service Connection in Azure DevOps
## Objective
### To securely connect Azure DevOps to external Azure resources (like Web Apps, ACR, or AKS) using a Service Connection, allowing pipelines to deploy applications seamlessly to Azure infrastructure.

## Steps Performed
### 1. Navigate to Service Connections
- Go to Project Settings → Service connections

- Click on “+ New service connection”

### 2. Choose Connection Type
- Selected Azure Resource Manager

- Authentication method: Service principal (automatic)

### 3. Configure Service Connection
- Subscription: Azure for Students

- Resource Group: mynewresource

- Service Connection Name: AzureAppServiceConnection



<img width="1918" height="854" alt="Image" src="https://github.com/user-attachments/assets/b3870b10-6c00-444f-8cbf-be76ab913509" />


### 4. Used in Pipeline
```bash
- task: AzureWebApp@1
  inputs:
    azureSubscription: 'AzureAppServiceConnection'
    appName: 'app-wallet-cwu'
    package: '$(Pipeline.Workspace)/drop/Wallet-0.0.1-SNAPSHOT.jar'
    appType: 'webAppLinux'
``` 

This task uses the created service connection to deploy the .jar package to Azure App Service.

<img width="1330" height="688" alt="Image" src="https://github.com/user-attachments/assets/3eae333e-2217-49bb-8898-511ff006a3bb" />
<img width="1377" height="372" alt="Image" src="https://github.com/user-attachments/assets/1d632147-c5e0-452c-b5b2-b66aff894daa" />

## Summary
The service connection setup allows secure communication between Azure DevOps and Azure services. It is a critical integration step for CI/CD pipelines to deploy artifacts automatically to the cloud without storing credentials manually.



