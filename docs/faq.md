# Frequently Asked Questions

## I have written CLI and Powershell scripts to deploy my solution instead of ARM templates, how will I be able to call these scripts to deploy my Managed app?
You can do that using [ARM deployment scripts](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deployment-script-template).

## My managed app solution is a web app and I would like configure it to use Azure AD login, how do I do that?
You need to configure you AD app registration for your web app.  For you to automate this, you would need to write a deployment script and provide a user-assigned managed identity with all the required permissions to perform actions defined in you script.  

The managed identity would need to be assigned to the [Application Administrator role](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#application-administrator) (or any custom AD role that has the permission to create application registration such as ‘microsoft.directory/applications/createAsOwner’ or ‘microsoft.directory/applications/create’, more on this [here](https://docs.microsoft.com/en-us/azure/active-directory/roles/custom-available-permissions)) and only the Global Administrator can do this.  

![Assign user-managed identity to AD role screenshot](/images/assignadrole.png)

Then, pass this managed identity as a parameter to the managed app thru the [Identity selector](https://docs.microsoft.com/en-us/azure/azure-resource-manager/managed-applications/microsoft-managedidentity-identityselector).
 

