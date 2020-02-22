

# Creating a Azure Function for Custom Resource Providers

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhasangural%2FCustomResourceProvider%2Fmaster%2Ftemplates%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>

This sample template deploys an Azure Function to Azure and creates essential function for Custom Resource Provider. It also creates a System Assigned Identity which is App Registration for using from Azure Function to handle authentication and authorisation process. When deployment is succeeded, you can get System Assigned Identity Id (Principal Id ) from the template output section. 

Let you know that your Azure Function name will be : 
####  https://{FuncName}.azurewebsites.net/ 

You need to give an access to the Managed Identity which is created by Azure Function ARM template.

# Requirements for Azure Function - Custom Resource Provides

*   Give access to Principal Id for Azure Subscription. At least It has to have Deployment/write permission.
*   Azure Resource Manager Template will be deployed AZ.Function v2. Do not change it.
    

# Registering and Using Custom Resource Provider

This sample deployment creates the following two resource on the Azure.

1) It is extended to be ARM resource called custom "ContainerProvider".
2) It is going to call API called "startContainer"

### Note: You need to update the Custom Resource Template to put your Azure Function URL.
```ruby
resourceTypes": [
                    {
                        "name": "startContainer",
                        "routingType": "proxy",
                        "endpoint": "https://customprovider-func.azurewebsites.net/api/{RequestPath}"
                    }
```

# Creating a Container Using Custom Resource Provider.


<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhasangural%2FCustomResourceProvider%2Fmaster%2Ftemplates%2FcustomContanier.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>




