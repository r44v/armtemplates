# armtemplates

A repo with public arm templates to link to azure devops services

# Updates

**20191108**

Reworked standard

* Added owner identifier
* removed dash between owner identifier and project name
* project name is now 7 characters
* Decreased environment to single character
* Increased resource-type with 1 character (now 4) and reworked short codes to fit standard

# Naming conventions

everyname should be limited to 24 characters

```
<owner-identifier(3)><project-name(7)>-<environment(1)>-<region(4)>-<resource-type(4)>-<instancenumber(1)>
```

## Examples

Some examples (resources required for moest webapps)
```
r44todoapp-t-weeu-rsgp-0
r44todoapp-t-weeu-wapp-0
r44todoapp-t-weeu-wasp-0
r44todoapp-t-weeu-msql-0
r44todoapp-t-weeu-mdbs-0

r44todoapp-p-weeu-rsgp-0
r44todoapp-p-weeu-wapp-0
r44todoapp-p-weeu-wasp-0
r44todoapp-p-weeu-msql-0
r44todoapp-p-weeu-mdbs-0
```

## project name

Make the project name 8 characters long and right pad with x's

## environment names

environments:
- d (Development)
- t (Testing)
- a (Acceptence)
- p (Production)

## Resource names

I got inspiration from (https://www.linkedin.com/pulse/azure-naming-calculator-nathan-smith) 

|Resource Type              |Short Code|
|---------------------------|----------|
|API Management             |apim      |
|App Service                |wapp      |
|App Service Plan           |wasp      |
|Azure App function         |fapp      |
|Azure Container Instance   |acix      |
|Azure Container registery  |acrx      |
|Azure Data Factory         |adfx      |
|Azure Kubertnetes Service  |aksx      |
|Azure MySQL Database       |msql      |
|Azure MySQL Server         |mdbs      |
|Azure Postgres Database    |psql      |
|Azure Postgres Server      |pdbs      |
|Azure SQL Databse          |asql      |
|Azure SQL Server           |adbs      |
|Azure Synapse Analytics    |adwh      |
|Cosmos DB                  |cosm      |
|Data Lake Storage          |lake      |
|Key Vault                  |keyv      |
|Network Interface          |nint      |
|Network Security Group     |nsgp      |
|Public IP Address          |pipx      |
|Resource Group             |rsgp      |
|Send Grid                  |sgrd      |
|Storage Account            |stor      |
|Subnet                     |snet      |
|Virtual Machine linux      |vmli      |
|Virtual Machine windows    |vmwi      |
|Virtual Network            |vnet      |

## Location names

Also some shortcodes for location names

|Location            |Short code|
|--------------------|----------|
|North Europe        |noeu      |
|West Europe         |weeu      |
|Germany North       |deno      |
|Germany West Central|dewc      |
|Central US          |cus1      |
|East US             |eus1      |
|East US 2           |eus2      |
|North Central US    |ncus      |
|South Central US    |scus      |
|West US             |wus1      |
|West US 2           |wus2      |
|West Central US     |wcus      |

# Notes

https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-functions
https://azure.microsoft.com/en-gb/global-infrastructure/regions/
https://docs.microsoft.com/en-us/azure/architecture/best-practices/naming-conventions
https://www.google.com/search?client=firefox-b-ab&q=germany+short+form

Some Azure RM commands for testing

```
Test-AzureRmResourceGroupDeployment -ResourceGroupName "" -TemplateFile "" -TemplateParameterFile ""
```
