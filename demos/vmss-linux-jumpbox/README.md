---
description: This template allows you to deploy a simple VM Scale Set of Linux VMs using the latest patched version of Ubuntu Linux 15.10 or 14.04.4-LTS. There is also a jumpbox to enable connections from outside of the VNet the VMs are in.
page_type: sample
products:
- azure
- azure-resource-manager
urlFragment: vmss-linux-jumpbox
languages:
- json
---
# Deploy a simple VM Scale Set with Linux VMs and a Jumpbox

![Azure Public Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/PublicLastTestDate.svg)
![Azure Public Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/PublicDeployment.svg)

![Azure US Gov Last Test Date](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/FairfaxLastTestDate.svg)
![Azure US Gov Last Test Result](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/FairfaxDeployment.svg)

![Best Practice Check](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/BestPracticeResult.svg)
![Cred Scan Check](https://azurequickstartsservice.blob.core.windows.net/badges/demos/vmss-linux-jumpbox/CredScanResult.svg)

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fdemos%2Fvmss-linux-jumpbox%2Fazuredeploy.json)
[![Deploy To Azure US Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.svg?sanitize=true)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fdemos%2Fvmss-linux-jumpbox%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fdemos%2Fvmss-linux-jumpbox%2Fazuredeploy.json)

This template allows you to deploy a simple VM Scale Set of Linux VMs using the latest patched version of Ubuntu Linux 15.10 or 14.04.4-LTS. This template also deploys a jumpbox with a public IP address in the same virtual network. You can connect to the jumpbox via this public IP address, then connect from there to VMs in the scale set via private IP addresses. To ssh into the jumpbox, you could use the following command:

ssh {username}@{jumpbox-public-ip-address}

To ssh into one of the VMs in the scale set, go to resources.azure.com to find the private IP address of the VM, make sure you are ssh'ed into the jumpbox, then execute the following command:

ssh {username}@{vm-private-ip-address}

PARAMETER RESTRICTIONS
======================

vmssName must be 3-61 characters in length. It should also be globally unique across all of Azure. If it isn't globally unique, it is possible that this template will still deploy properly, but we don't recommend relying on this pseudo-probabilistic behavior.
instanceCount must be 100 or less.

`Tags: Microsoft.Network/networkSecurityGroups, Microsoft.Network/virtualNetworks, Microsoft.Storage/storageAccounts, Microsoft.Network/publicIPAddresses, Microsoft.Network/networkInterfaces, Microsoft.Compute/virtualMachines, Microsoft.Compute/virtualMachineScaleSets`
