---
description: This template allows you to deploy a simple Ubuntu VM Scale Set integrated with Azure Application Gateway, and supports up to 1000 VMs
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: vmss-ubuntu-app-gateway
languages:
- json
---
# Deploy an Ubuntu VM scale set with Azure Application Gateway

![Azure Public Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/PublicLastTestDate.svg)
![Azure Public Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/PublicDeployment.svg)

![Azure US Gov Last Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/FairfaxLastTestDate.svg)
![Azure US Gov Last Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/FairfaxDeployment.svg)

![Best Practice Check](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/BestPracticeResult.svg)
![Cred Scan Check](https://azurequickstartsservice.blob.core.windows.net/badges/quickstarts/microsoft.compute/vmss-ubuntu-app-gateway/CredScanResult.svg)

This template deploys an Ubuntu VM Scale Set integrated with Azure Application Gateway.

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.compute%2Fvmss-ubuntu-app-gateway%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.compute%2Fvmss-ubuntu-app-gateway%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.compute%2Fvmss-ubuntu-app-gateway%2Fazuredeploy.json)

The Application Gateway is configured for round robin load balancing of incoming connections at port 80 (of the gateway's public IP address) to VMs in the scale set.

Note that this template does not install an application on the VM Scale Set VMs, so if you want to demonstrate the round robin load balancing, the template will need to be updated (for example by adding an extension to install a web server).

This template supports VM scale sets of up to 1,000 VMs, and uses Azure Managed Disks.

`Tags: Microsoft.Network/virtualNetworks, Microsoft.Network/publicIPAddresses, Microsoft.Network/applicationGateways, Microsoft.Compute/virtualMachineScaleSets`
