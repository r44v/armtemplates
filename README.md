# armtemplates

A repo with public arm templates to link to azure devops services and a naming standard.

# Naming conventions

every resource name should be limited to 24 characters.

```
<owner-identifier(3)><project-name(7)>-<environment(1)>-<region(4)>-<resource-type(4)>-<instancenumber(1)>
```

## Examples

Some examples (resources required for most webapps)
```
r44todoapp-t-weeu-rsgp-0
r44todoapp-t-weeu-wapp-0
r44todoapp-t-weeu-wasp-0
r44todoapp-t-weeu-mdbs-0
r44todoapp-t-weeu-msql-0

r44todoapp-p-weeu-rsgp-0
r44todoapp-p-weeu-wapp-0
r44todoapp-p-weeu-wasp-0
r44todoapp-p-weeu-mdbs-0
r44todoapp-p-weeu-msql-0
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
|Application Insight        |ains      |
|App Service                |wapp      |
|App Service Plan           |wasp      |
|Azure App function         |fapp      |
|Azure Container Instance   |acix      |
|Azure Container registery  |acrx      |
|Azure Data Factory         |adfx      |
|Azure Kubertnetes Service  |ak8s      |
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
|Text Analytics             |txta      |
|Virtual Network            |vnet      |

**Exceptions**

|Resource Type              |Short Code|
|---------------------------|----------|
|Virtual Machine windows    |vm        |
|Virtual Machine linux      |vm        |

## Virtual machines

The VM Name must be between 4 and 12 characters long and contain letters, numbers and hyphens only.

```
projectdvm0
projectdvm1
projecttvm0
projectavm0
projectpvm0
```

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


# CHANGELOG

[20200515]
* [Changed] resource names. All virtualmachines are now `vm`
* [Changed] resource names. Public Ip Address changed from `pipx` to `pipa`

[20191108]
* [Changed] standard
* [Removed] dash between owner identifier and project name
* [Added] owner identifier
* [Changed] project name. Now 7 characters
* [Changed] environment. Decreased to single character
* [Changed] resource-type. Increased with 1 character (now 4) and reworked short codes to fit standard

[Unchanged]
* Keep actual version numbers for the standard
* Contemplate changing `aksx` to `ak8s`

**Changelog standard**

Based on (https://keepachangelog.com/en/1.0.0/)[Keep a changelog]

Types of changes
* [Added] for new features.
* [Changed] for changes in existing functionality.
* [Deprecated] for soon-to-be removed features.
* [Removed] for now removed features.
* [Fixed] for any bug fixes.
* [Security] in case of vulnerabilities.


# Notes

https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-functions
https://azure.microsoft.com/en-gb/global-infrastructure/regions/
https://docs.microsoft.com/en-us/azure/architecture/best-practices/naming-conventions
https://www.google.com/search?client=firefox-b-ab&q=germany+short+form

Some Azure RM commands for testing

```
Test-AzureRmResourceGroupDeployment -ResourceGroupName "" -TemplateFile "" -TemplateParameterFile ""
```
