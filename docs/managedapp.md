# Azure Application - Managed Application
#### [prev](./saastransact.md) | [home](./welcome.md)  | [next](./references.md)
- Solution template plans, on the other hand, are non-transactable in the commercial marketplace but can be used to deploy paid VMs. Use this when the customer will manage the solution and transactions are build through another plan.
- Managed Application (aka Manage App) is a type of Azure Application offer plan to publish solution to the commercial marketplace that is transactable, used to deploy solution into the customer's subscription that will be managed by the partner/publisher.  
- We will focus on creating and publishing Managed App.

## Listing Options
- Get It Now
- Test Drive

## Publish flow
- Managed applications are by default transactable
- To add Testdrive to any offer = Republish offer

## Prequisites 
- Familiar with ARM
- Familiar with Azure Managed Applications

## Technical configuration
- For managed applications that emit metering events using the Marketplace metering service APIs, you must provide the identity that your service will use when emitting metering events.
- Create an Azure Active Directory (AAD) app, you need to share your AAD Direcotry (tenant) ID and AAD application ID.
- AAD application ID will be associated to your publisher ID and can only be re-used within this publisher account.


## Demo
![Managed App Options](/images/manage_app_options.png)
- Creating Managed Application, and test publish this internally as a Service Catalog App - [Quickstart: Create and publish a managed application definition](https://docs.microsoft.com/en-us/azure/azure-resource-manager/managed-applications/publish-service-catalog-app?tabs=azure-powershell)
- Once you have the Managed Application and its deployable package, you can proceed to [create Azure application offer](https://docs.microsoft.com/en-us/azure/marketplace/create-new-azure-apps-offer) in the Commercial Marketplace.
- As a publisher, ensure that you keep track of all your customer subscriptions by setting up [customer usage attribution](https://docs.microsoft.com/en-us/azure/marketplace/azure-partner-customer-usage-attribution)
