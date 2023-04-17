Deploy Azure Managed Application using Azure CLI 

Modify the snippet below to deploy the Managed Application definition to a Resource Group in your Azure subscription.

az managedapp definition create \
  --name "MinimalTemplate" \
  --location <rgLocation> \
  --resource-group <yourRgName> \
  --lock-level ReadOnly \
  --display-name "Minimal Template" \
  --description "A minimal template" \
  --authorizations "<userOrGroupId>:<RBACRoleDefinitionId>" \
  --package-file-uri "https://raw.githubusercontent.com/kar122/aks-app/main/Managed Application Packages/1-Managed-AKS/app.zip"
