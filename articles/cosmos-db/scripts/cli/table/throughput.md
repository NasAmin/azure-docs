---
title: Perform throughput (RU/s) operations for Azure Cosmos DB Table API resources
description: Azure CLI scripts for throughput (RU/s) operations for Azure Cosmos DB Table API resources
author: markjbrown
ms.author: mjbrown
ms.service: cosmos-db
ms.subservice: cosmosdb-table
ms.topic: sample
ms.date: 02/21/2022
---

# Throughput (RU/s) operations with Azure CLI for a table for Azure Cosmos DB Table API

[!INCLUDE[appliesto-table-api](../../../includes/appliesto-table-api.md)]

The script in this article creates a Table API table then updates the throughput the table. The script then migrates from standard to autoscale throughput then reads the value of the autoscale throughput after it has been migrated.

[!INCLUDE [quickstarts-free-trial-note](../../../../../includes/quickstarts-free-trial-note.md)]

[!INCLUDE [azure-cli-prepare-your-environment.md](../../../../../includes/azure-cli-prepare-your-environment.md)]

- This article requires version 2.12.1 or later. Run `az --version` to find the version. If you need to install or upgrade, see [Install Azure CLI](/cli/azure/install-azure-cli). If using Azure Cloud Shell, the latest version is already installed.

## Sample script

[!INCLUDE [cli-launch-cloud-shell-sign-in.md](../../../../../includes/cli-launch-cloud-shell-sign-in.md)]

### Run the script

:::code language="azurecli" source="~/azure_cli_scripts/cosmosdb/table/throughput.sh" range="4-57":::

## Clean up resources

[!INCLUDE [cli-clean-up-resources.md](../../../../../includes/cli-clean-up-resources.md)]

```azurecli
az group delete --name $resourceGroup
```

## Sample reference

This script uses the following commands. Each command in the table links to command specific documentation.

| Command | Notes |
|---|---|
| [az group create](/cli/azure/group#az_group_create) | Creates a resource group in which all resources are stored. |
| [az cosmosdb create](/cli/azure/cosmosdb#az_cosmosdb_create) | Creates an Azure Cosmos DB account. |
| [az cosmosdb table create](/cli/azure/cosmosdb/table#az_cosmosdb_table_create) | Creates an Azure Cosmos Table API table. |
| [az cosmosdb table throughput update](/cli/azure/cosmosdb/table/throughput#az_cosmosdb_table_throughput_update) | Update throughput for an Azure Cosmos Table API table. |
| [az cosmosdb table throughput migrate](/cli/azure/cosmosdb/table/throughput#az_cosmosdb_table_throughput_migrate) | Migrate throughput for an Azure Cosmos Table API table. |
| [az group delete](/cli/azure/resource#az_resource_delete) | Deletes a resource group including all nested resources. |

## Next steps

For more information on the Azure Cosmos DB CLI, see [Azure Cosmos DB CLI documentation](/cli/azure/cosmosdb).
