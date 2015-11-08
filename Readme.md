## Step by step tutorial to deploy MongoDb on Windows Azure using Azure Resource Manager template deployment
Most of these templates are based on https://github.com/Azure/azure-quickstart-templates
The effort in this repo is to provide a list of templates where you can learn linearly about Azure Resource Manager template deployment toward having MongoDB running on Windows Azure.

- [templates/100.simplevm.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/100.simplevm.json) is to create a Linux IaaS vm with a vnet, public ip address, and a NIC using Ubuntu 14.04.2-LTS image.
- Based on previous template, [templates/101.ubuntu_with_mongo.json](https://github.com/weinong/MongoOnAzure/blob/master/templates/101.ubuntu_with_mongo.json) includes a custom script extension which downloads and executes a script from github to install MongoDb.
