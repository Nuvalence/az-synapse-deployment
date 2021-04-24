# Automated Synapse Deployment

The following repository allows you to easily deploy an [Azure Synapse](https://docs.microsoft.com/en-us/azure/synapse-analytics/get-started-create-workspace) Workspace to your Azure Account.

## Pre-requisites

* Azure account

## Resources Created During Deployment

* Storage Account V2
* Azure Synapse Workspace (this includes the necessary SQL and Spark backends)


## Steps

Simply click on the **Deploy to Azure** button to kick off the deployment process.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FNuvalence%2Faz-synapse-deployment%2Fmaster%2Fdeploymentfiles%2Fsynapsedeployment.json)

### Parameters Description

| Name | Description | 
| ---- | ----------  |
| Storage Account Name | Name of the storage account resource. Storage account names must be between 3 and 24 characters in length and may contain numbers and lowercase letters only. Your storage account name must be unique within Azure. No two storage accounts can have the same name. |
| Sql Administrator Login | Login name provisioned for the SQL Server used by Azure Synapse |
| Sql Administrator Password | Password provisioned for the SQL Server used by Azure Synapse. Your Azure account migh have specific password policies that can affect this resource |
| Synapse Name | Azure Synpase instance name |
| Sql Sku | SQL Server SKUs configured for Azure Synapse. A description of each SKU can be found [here](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/memory-concurrency-limits#service-levels) |
|Role Name Guid | This ID is generated at runtime and used to configure the permissions for Azure Synapse. **DO NOT UPDATE THE VALUE** |
