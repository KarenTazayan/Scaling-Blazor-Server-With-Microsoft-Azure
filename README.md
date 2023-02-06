## Scaling Blazor Server with Microsoft Azure

### 1. Prepare Azure DevOps and initialize the solution repo.

1. Open Azure DevOps portal : https://dev.azure.com/
2. Create new organization/use an existing organization. A sample name: **scaling-blazor-server-1**
3. Create a new public project. A sample name: **ShoppingApp**.
4. Import existing repository: https://github.com/KarenTazayan/Scaling-Blazor-Server-With-Microsoft-Azure
5. Create YAML pipeline. A sample name: Default CI and CD pipeline

### 2. Create a self-hosted agents pool for Azure DevOps organization.

### 3. Create a Azure service connection.

Cretae a new Azure service connection, name: **DefaultAzureServiceConnection**.
az ad sp create-for-rbac --name Scaling-Blazor-Server-1

Install [GitTools](https://marketplace.visualstudio.com/items?itemName=gittools.gittools) for the current Azure DevOps Organization.

Disable [shallow fetch](https://learn.microsoft.com/en-us/azure/devops/pipelines/yaml-schema/steps-checkout?view=azure-pipelines#shallow-fetch) the Azure Pipeline. It's required for GitTools.