# SaaS Offer 
#### [prev](./concepts.md) | [home](./welcome.md)  | [next](./saaspricing.md)
## Listing Options
- Contact Me 
- Free Trial
- Get it now (Free)
- Sell through Microsoft (aka Transactable, SaaS Transact)

## Test Drive
- Test drives give customers access to a **preconfigured environment** for a fixed number of hours.
- This includes a hands-on, self-guided tour of your product’s key features and benefits being demonstrated in a real-world implementation scenario.
- You can offer Test Drives across all listing, including Free Trial.

## Upgrade flow
- Contact Me -> Trial = Re-publish offer 
- Contact Me -> Transact = Create new offer
- Trial -> Transact = Create New Offer
- To add Test Drive to any offer = Re-publish offer

## Minimum technical requirements for Contact Me
- Connect to the CRM system to managed [customer leads](https://docs.microsoft.com/en-us/azure/marketplace/partner-center-portal/commercial-marketplace-get-customer-leads#connect-to-your-crm-system).
  - Dynamics 365 for Customer Engagement
  - Marketo
  - Salesforce
  - Azure Table 
  - HTTPS endpoint in Power Automate

## Minimum technical requirements for Free Trial, Get it Now, Transact
- Your SaaS application must be a multitenant solution.
- You must create a landing page. After a user purchases your offer, they’re directed to the landing page. This helps them complete any additional provisioning or setup that/s required. 
  - [Build the landing page for your transactable SaaS offer in the commercial marketplace](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-transactable-saas-landing-page)
  - [Build the landing page for your free or trial SaaS offer in the commercial marketplace](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-free-or-trial-landing-page)
- Landing page must be available 24/7, otherwise your buyers will not be able to activate their subscription.

## Additional technical requirements for Transact
- Azure AD with single sign-on (SSO) identity management and authentication is required for the buying user accessing the landing page. More on this [here](https://docs.microsoft.com/en-us/azure/marketplace/azure-ad-saas)
- You must use the SaaS Fulfillment APIs to integrate with Azure Marketplace and Microsoft AppSource. You must expose a service that can interact with the SaaS subscription to create, update, and delete a user account and service plan. Critical API changes must be supported within 24 hours. Non-critical API changes will be released periodically. Diagrams and detailed explanations describing the usage of the collected fields are available in documentation for the APIs.
- You must create Connection webhook with an HTTPS endpoint.  This is called by Microsoft by using the POST HTTP call to notify the publisher side of following events that happen on the Microsoft side.
- You must create at least one plan for your offer. Your plan is priced based on the pricing model you select before publishing: flat rate or per-user. More details about plans are provided later in this article.
- The customer can cancel your offer at any time.

More details [here](https://docs.microsoft.com/en-us/azure/marketplace/plan-saas-offer#technical-requirements)

![SaaS Moving Parts - AD Requirements](/images/saasmovingparts.png)

##  Creating SaaS Offer Listing - Demo
- Configuring Sample Customer Provisioning App, based from the reference example in [Microsoft Commercial Marketplace - Community Sample Code and SDK for SaaS Applications](https://github.com/Azure/Microsoft-commercial-marketplace-transactable-SaaS-offer-SDK)

## SaaS SDK Lifecycle
![SaaS SDK Lifecycle](https://docs.microsoft.com/en-us/azure/marketplace/partner-center-portal/media/saas-subscription-lifecycle-api-v2.png)

## Architecture Choices

![SaaS Architectural Choices](/images/archchoices.png)


## Best Practices
### DEV and PROD offers
- Plan creating two offers: test and development (DEV) and production (PROD) 
- With DEV
  - Have the same marketing language as the PROD
  - Add preview users
  - Add plans/meters with $0
  - Publish
  - **DO NOT GO LIVE!**
  
  ![SaaS Preview Offer](/images/previewoffer.png)
- With PROD
  - Replicate marketing content
  - Add real plans
  - Publish

More details [here](https://docs.microsoft.com/en-us/azure/marketplace/create-saas-dev-test-offer)




