Creating a Azure Function for Custom Resource Providers

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-custom-providers%2Fmaster%2FCustomRPWithFunction%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>

This sample template deploys a custom resource provider to azure and creates a user using an ARM template. 

The customproviders resource is a hidden azure resources so to confirm that the resource provider has been deployed you will have to check the box that says Show hidden types in the azure portal browse page for the resource group.
![](images/showhidden.png)


# Details on the custom resource provider created. 

This sample deployment creates the following two apis on the resource. 

1) An ARM extended resource called "users"
2) An API called "ping"

### Users 

The users resource is defined in the following part of the ARM template : 
