# azurecli
azure cli documentation 

Azure cli is a command line tool that enable one to create and manage azure resources. It is a cross platform, installable on windows,macos, Linux.

It runs in windows powerShell, cmd or Bash and other Unix shells.



Azure CLI syntax is similar to that of Bash scripting. If one work primarily with Linux systems, Azure CLI feels more natural.

# Command Lists :--


**Version, Help**

| **Command**       | **Azure CLI** |
|-------------------|---------------|
| Find Version      | az --version  |
| Get Help          | az --help     |
| View Command Help | az vm --help  |


**Sign in , Subscription,and Location Commands**


| **Command**                 | **Azure CLI**                                  |
|-----------------------------|------------------------------------------------|
| Sign in with Web Browser    |  az login                                      |
| Get available subscriptions | az account list                                |
| Set Subscription            | az account set –-subscription <SubscriptionId> |
| List Azure Locations        | az account list-locations                      |


**Resource Group, VM and Storage**

| **Command**                  | **Azure CLI**                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Create Resource Group        | az group create --name <ResourceGroupName> --location eastus                                                                                     |
| Create Azure Virtual Machine | az vm create --resource-group myResourceGroup --name myVM --image UbuntuLTS --admin-username azureuser --admin-password '<Password>'             |
| Create Azure Storage Account | az storage account create --name <StorageAccountName> --resource-group <ResourceGroupName> --location eastus --sku Standard_LRS --kind StorageV2 |


**Virtual Machine**

| **Command**          | **Azure CLI**                                                     |
|----------------------|-------------------------------------------------------------------|
| List VM              | az vm List                                                        |
| Restart VM           | az vm restart --name myVM --resource-group <ResourceGroupName>    |
| Stop VM              | az vm stop --name myVM --resource-group <ResourceGroupName>       |
| Stop & Deallocate VM | az vm deallocate --name myVM --resource-group <ResourceGroupName> |
| Start VM             | az vm start --name myVM --resource-group <ResourceGroupName>      |
| Delete VM            | az vm delete --name myVM --resource-group <ResourceGroupName>     |


**Properties and Output**

| **Command**                       | **Azure CLI**            |
|-----------------------------------|--------------------------|
| Show all subscription information | az account list --all    |
| Output as a Table                 | az account list -o table |
| Output as JSON                    | az account show          |