# Azure Application - Managed Application

- Managed Application (aka Manage App) is a type of Azure Application offer plan to publish solution to the commercial marketplace that is transactable, used to deploy solution into the customer's subscription that will be managed by the partner/publisher.
- Solution template plans, on the other hand, are non-transactable in the commercial marketplace but can be used to deploy paid VMs. 
- We will focus on creating and publishign Managed App.

## Listing Options
- Contact Me 
- Free Trial
- Get it now (Free)
- Sell through Microsoft (aka Transactable, SaaS Transact)

## Listing Options
- Contact Me 
- Free Trial
- Get it now (Free)
- Sell through Microsoft (aka Transactable, SaaS Transact)

## Upgrade flow
- Contact Me -> Trial = Repulish offer 
- Contact Me -> Transact = Create new offer
- Trial -> Transact = Create New Offer
- To add Testdrive to any offer = Republish offer

## Minimum technical requirements for Contact Me
- There's none, aside from just connecting to the CRM system to managed [customer leads](https://docs.microsoft.com/en-us/azure/marketplace/plan-saas-offer#customer-leads).

## Minimum technical requirements for Free Trial, Get it Now, Transact
- Your SaaS application must be a multitenant solution.
- You can enable both Microsoft Accounts (MSA) and Azure Active Directory (Azure AD) for authenticating users.
- You must create a landing page. After a user purchases your offer, they’re directed to the landing page. This helps them complete any additional provisioning or setup that/s required. 
[Build the landing page for your transactable SaaS offer in the commercial marketplace]
[Build the landing page for your free or trial SaaS offer in the commercial marketplace]

## Additional technical requirements for Transact
- Azure AD with single sign-on (SSO) identity management and authentication is required for the buying user accessing the landing page. More on this [here](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-saas)
- You must use the SaaS Fulfillment APIs to integrate with Azure Marketplace and Microsoft AppSource. You must expose a service that can interact with the SaaS subscription to create, update, and delete a user account and service plan. Critical API changes must be supported within 24 hours. Non-critical API changes will be released periodically. Diagrams and detailed explanations describing the usage of the collected fields are available in documentation for the APIs.
- You must create at least one plan for your offer. Your plan is priced based on the pricing model you select before publishing: flat rate or per-user. More details about plans are provided later in this article.
- The customer can cancel your offer at any time.

More details [here](https://docs.microsoft.com/en-us/azure/marketplace/plan-saas-offer#technical-requirements)

## Demo
- Creating SaaS Transact offer listing
- Configuring Sample Customer Provisioning App, based from the reference example in [Microsoft Commercial Marketplace - Community Sample Code and SDK for SaaS Applications](https://github.com/Azure/Microsoft-commercial-marketplace-transactable-SaaS-offer-SDK)
