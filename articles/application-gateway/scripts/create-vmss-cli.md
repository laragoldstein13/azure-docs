---
title: Azure CLI Script Sample - Manage web traffic | Microsoft Docs
description: Azure CLI Script Sample - Manage web traffic with an application gateway and a virtual machine scale set.
services: application-gateway
author: greg-lindsay
tags: azure-resource-manager
ms.service: application-gateway
ms.topic: sample
ms.tgt_pltfrm: vm-windows
ms.workload: infrastructure
ms.date: 01/29/2018
ms.author: greglin
ms.custom: mvc, devx-track-azurecli
---

# Manage web traffic using the Azure CLI

This script creates an application gateway that uses a virtual machine scale set for backend servers. The application gateway can then be configured to manage web traffic. After running the script, you can test the application gateway using its public IP address.

[!INCLUDE [sample-cli-install](../../../includes/sample-cli-install.md)]

[!INCLUDE [quickstarts-free-trial-note](../../../includes/quickstarts-free-trial-note.md)]

## Sample script

[!code-azurecli-interactive[main](../../../cli_scripts/application-gateway/create-vmss/create-vmss.sh "Create application gateway")]

## Clean up deployment 

Run the following command to remove the resource group, application gateway, and all related resources.

```azurecli-interactive 
az group delete --name myResourceGroupAG --yes
```

## Script explanation

This script uses the following commands to create the deployment. Each item in the table links to command specific documentation.

| Command | Notes |
|---|---|
| [az group create](/cli/azure/group) | Creates a resource group in which all resources are stored. |
| [az network vnet create](/cli/azure/network/vnet) | Creates a virtual network. |
| [az network vnet subnet create](/cli/azure/network/vnet/subnet#az-network-vnet-subnet-create) | Creates a subnet in a virtual network. |
| [az network public-ip create](/cli/azure/network/public-ip) | Creates the public IP address for the application gateway. |
| [az network application-gateway create](/cli/azure/network/application-gateway) | Create an application gateway. |
| [az vmss create](/cli/azure/vmss) | Creates a virtual machine scale set. |
| [az network public-ip show](/cli/azure/network/public-ip) | Gets the public IP address of the application gateway. |

## Next steps

For more information on the Azure CLI, see [Azure CLI documentation](/cli/azure/overview).

Additional application gateway CLI script samples can be found in the [Azure Windows VM documentation](../cli-samples.md).
