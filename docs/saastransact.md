# SaaS Offer 
#### [prev](./concepts.md) | [home](./welcome.md)  | [next](./managedapp.md)
## Listing Options
- Contact Me 
- Free Trial
- Get it now (Free)
- Sell through Microsoft (aka Transactable, SaaS Transact)

## Upgrade flow
- Contact Me -> Trial = Re-publish offer 
- Contact Me -> Transact = Create new offer
- Trial -> Transact = Create New Offer
- To add Test Drive to any offer = Re-publish offer

## Minimum technical requirements for Contact Me
- There's none, aside from just connecting to the CRM system to managed [customer leads](https://docs.microsoft.com/en-us/azure/marketplace/plan-saas-offer#customer-leads).

## Minimum technical requirements for Free Trial, Get it Now, Transact
- Your SaaS application must be a multitenant solution.
- You can enable both Microsoft Accounts (MSA) and Azure Active Directory (Azure AD) for authenticating users.
- You must create a landing page. After a user purchases your offer, they’re directed to the landing page. This helps them complete any additional provisioning or setup that/s required. 
[Build the landing page for your transactable SaaS offer in the commercial marketplace](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-transactable-saas-landing-page)
[Build the landing page for your free or trial SaaS offer in the commercial marketplace](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-free-or-trial-landing-page)

## Additional technical requirements for Transact
- Azure AD with single sign-on (SSO) identity management and authentication is required for the buying user accessing the landing page. More on this [here](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-saas)
- You must use the SaaS Fulfillment APIs to integrate with Azure Marketplace and Microsoft AppSource. You must expose a service that can interact with the SaaS subscription to create, update, and delete a user account and service plan. Critical API changes must be supported within 24 hours. Non-critical API changes will be released periodically. Diagrams and detailed explanations describing the usage of the collected fields are available in documentation for the APIs.
- You must create at least one plan for your offer. Your plan is priced based on the pricing model you select before publishing: flat rate or per-user. More details about plans are provided later in this article.
- The customer can cancel your offer at any time.

More details [here](https://docs.microsoft.com/en-us/azure/marketplace/plan-saas-offer#technical-requirements)

![SaaS Moving Parts - AD Requirements](/images/saasmovingparts.png)

## Demo
- Creating SaaS Transact offer listing
- Configuring Sample Customer Provisioning App, based from the reference example in [Microsoft Commercial Marketplace - Community Sample Code and SDK for SaaS Applications](https://github.com/Azure/Microsoft-commercial-marketplace-transactable-SaaS-offer-SDK)

