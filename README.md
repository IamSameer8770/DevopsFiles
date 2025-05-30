
//Basic ARM Template for Storage account creation 
{
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "stgname": {
            "type": "string",
            "metadata": {
                "description": "name of storage account"
            }
        },
        "stgloc": {
            "type": "string",
            "metadata": {
                "description": "location of storage account"
            }
        },
        "stgsku": {
            "type": "string", 
            "metadata": {
                "description": "sku of storage account"
            }
        }
        
    },
    "functions": [],
    "variables": {},
    "resources": [
        {
            "name": "[parameters('stgname')]",
            "type": "Microsoft.Storage/storageAccounts",
            "apiVersion": "2023-05-01",
            "location": "[parameters('stgloc')]",
            "kind": "StorageV2",
            "sku": {
                "name": "[parameters('stgsku')]",
                "tier": "Standard"
            }
        }
    ],
    "outputs": {}
}
