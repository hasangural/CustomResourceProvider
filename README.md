# Creating a Azure Function for Custom Resource Providers

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhasangural%2FCustomResourceProvider%2Fmaster%2Ftemplates%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>

This sample template deploys an Azure Function to Azure and creates essential function for Custom Resource Provider. It also creates a System Assigned Identity which is App Registration for using from Azure Function to handle authentication and authorisation process. When deployment is succeeded, you can get System Assigned Identity Id (Principal Id ) from the template output section. 

Let you know that your Azure Function name will be : 
####  https://{FuncName}.azurewebsites.net/ 

You need to give an access to the Managed Identity which is created by Azure Function ARM template. You can get Principal Id.


# Details on the custom resource provider created. 

This sample deployment creates the following two apis on the resource. 

1) An ARM extended resource called "users"
2) An API called "ping"

### Users 

The users resource is defined in the following part of the ARM template : 
