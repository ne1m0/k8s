# Kubernetes

## Background
Includes...
- Azure Kubernetes Service - AKS-Engine template
- Google - GKE (in progress)

## Design

### Deploy AKS-Engine

aks-engine.exe generate .\kubernetes-windows.json --force-overwrite

### Then deploy the ARM template...

Login-AzureRMAccount

Set-AzureRMContext "subscription name"

New-AzureRmResourceGroupDeployment -ResourceGroupName "aksengine-rg" -TemplateFile "./_output/aksengine-01/azuredeploy.json" -TemplateParameterFile "./_output/aksengine-01/azuredeploy.parameters.json"
