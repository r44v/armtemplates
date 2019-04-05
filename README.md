# armtemplates
A repo with public arm templates to link to azure devops services

# Naming conventions

I prefer having all project related resources in the same resource group and having the same regional location for these resourses.

everyname should be limited to 24 characters

```
<project-name(8)>-<environment(4)>-<region(4)>-<resource-type(3)>-<instancenumber(1)>
```

## Examples

Some examples
```
vmtestxx-test-weeu-rsg-0
vmtestxx-test-weeu-vml-0
vmtestxx-test-weeu-vnt-0
vmtestxx-test-weeu-pip-0
```

## project name

Make the project name 8 characters long and right pad with x's

## environment names

environments:
- dev1 (Development + number)
- test (Testing)
- accp (Acceptence)
- stag (Staging)
- prod (Production)

## Resource names

I got inspiration from (https://www.linkedin.com/pulse/azure-naming-calculator-nathan-smith) 

|Resource Type              |Short Code|
|---------------------------|----------|
|Resource Group             |rsg       |
|Virtual Machine(linux/win) |vml/vmw   |
|Storage Account            |stg       |
|Virtual Network            |vnt       |
|Subnet                     |snt       |
|Network Interface          |nif       |
|Network Security Group     |nsg       |
|Public IP Address          |pip       |
|App Service                |app       |
|App Service Plan           |asp       |
|Key Vault                  |kvt       |
|Cosmos DB                  |cdb       |
|Azure SQL Server           |sql       |

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
