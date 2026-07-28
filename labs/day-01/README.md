# Day 01 - Azure Subscription Baseline

## Business scenario

TicoCloud Solutions assigned a new Azure subscription for controlled
learning and internal development.

## Objectives

- Audit the Azure subscription
- Configure cost monitoring
- Validate Azure CLI
- Deploy a tagged resource group
- Test the resource lifecycle

## Architecture

No workload resources were deployed during this lab.

## Commands used
***
Login
az version
az --help
az account --help
az login

***
Ver cuenta
az account show --output table
az account list --output table
az account show
az account show --output table
az account show `
  --query "{Subscription:name, State:state, IsDefault:isDefault}" `
  --output table
az account list-locations `
  --query "[].{Name:name,DisplayName:displayName}" `
  --output table

***
Ciclo de vida de Grupos de Recursos
az group create `
  --name rg-cloudjourney-dev-001 `
  --location eastus `
  --tags Environment=Lab Owner=Robin Project=CloudSupportJourney CostCenter=Learning
az group show `
  --name rg-cloudjourney-dev-001 `
  --output table
az group show `
  --name rg-cloudjourney-dev-001 `
  --query "{Name:name,Location:location,State:properties.provisioningState}" `
  --output table
***
Etiquetas de recursos
az tag update `
  --resource-id $resourceGroupId `
  --operation Merge `
  --tags ExpirationDate=2026-07-28
az tag update --operation Merge agrega o actualiza tags conservando las existentes. En cambio, az tag create puede reemplazar el conjunto completo de tags, una diferencia peligrosa en automatizaciones.

***
Eliminar Resource Group
az group delete `
  --name rg-cloudjourney-dev-001 `
  --yes

az group exists --name rg-cloudjourney-dev-001

## Troubleshooting

Title: Invalid resource group query
Severity: SEV-4
Impact: No customer impact
Assigned team: Cloud Operations

***
Prompt
Ejecuta intencionalmente:
az group show `
  --name rg-cloudjourney-prod-001 `
  --output table

***
Error mostrado en PowerShell
(ResourceGroupNotFound) Resource group 'rg-cloud-journey-prod-001' could not be found.
Code: ResourceGroupNotFound
Message: Resource group 'rg-cloud-journey-prod-001' could not be found.

***
Para resolverlo se ejecutó un comando para mostrar la lista de grupos de recursos existentes, se demostró que el recurso no existe.

az group exists --name rg-cloudjourney-prod-001

## Lessons learned

To be completed.

## Cost and cleanup

To be completed.

## English summary

To be completed.
