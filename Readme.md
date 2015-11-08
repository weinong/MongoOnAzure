## Step by step tutorial to deploy MongoDb on Windows Azure using Azure Resource Manager template deployment
This repo is created mainly for my own education. Most of these templates are based on https://github.com/Azure/azure-quickstart-templates, and they are organized linearly by their prefix in ascending order.

To deploy the template, you can use either [Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/powershell-install-configure/) or [Azure CLI](https://azure.microsoft.com/en-us/documentation/articles/xplat-cli/).  

- [templates/100.simplevm.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/100.simplevm.json) is to create a Linux IaaS vm with a vnet, public ip address, and a NIC using Ubuntu 14.04.2-LTS image.
- [templates/101.simplevm_with_datadisk.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/101.simplevm_with_datadisk.json) creates a Linux vm with a data disk. You need to follow the [doc](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-linux-how-to-attach-disk/) to partition, to format, and to mount the data disk manually.
- [templates/102.vm_with_datadisk_mounted.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/102.vm_with_datadisk_mounted.json) utilizes [the script from Azure's repo](https://github.com/Azure/azure-quickstart-templates/blob/master/shared_scripts/ubuntu/vm-disk-utils-0.1.sh) to partition, to format, and to mount the data disk automatically.
- [templates/200.ubuntu_with_mongo.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/200.ubuntu_with_mongo.json) includes a custom script extension which downloads and executes a script from github to install MongoDb.
