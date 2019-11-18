# Creating a Azure Function for Custom Resource Providers

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhasangural%2FCustomResourceProvider%2Fmaster%2Ftemplates%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>

This sample template deploys a Azure Function to Azure and creates basic function for Custom Resource Provider


# Details on the custom resource provider created. 

This sample deployment creates the following two apis on the resource. 

1) An ARM extended resource called "users"
2) An API called "ping"

### Users 

The users resource is defined in the following part of the ARM template : 
