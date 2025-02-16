---
title: Contracts
sidebar: Handbook
showTitle: true
---

# Annual plans and more

For customers who want to sign up for an annual (or longer) plan there is some additional paperwork needed to capture their
contractual commitment to a minimum term, and likely custom pricing as well.  At a minimum, they should sign an Order Form 
which references our standard [terms](/terms) and [privacy notice](/privacy).  In addition, they may want a custom Master Services Agreement (MSA) 
or Data Processing Agreement (DPA)

> If a customer wants to vary either our DPA, BAA or MSA terms it is a substantial effort for our legal team to review these changes.  At a minimum we should only do this for contracts above $20k a year, and even higher if they are asking for big changes (e.g. adding Service Level Agreements)

In addition, customers requiring our Enterprise plan are required to sign up for a minimum of $20k of PostHog Cloud Credit for a year, as well as adding the Teams plan to their subscription.

## Discounts

Our standard monthly [pricing](/pricing) has volume discounts built in, and we offer a pretty generous 20% discount for annual paid up-front plans, but some customers may ask for more.  This table outlines what we would require in return (bigger spend/longer commitment) to secure that bigger discount.

| Minimum Spend | 1 Year | 2 Year | 3 Year |
|---------------|--------|--------|--------|
| $20,000 | 20% | 25% | 30% |
| $60,000 | 25% | 30% | 35% |
| $100,000 | 30% | 35% | 40% |

Also note that the minimum amounts here are _after_ discounts e.g. they will need to purchase a minimum of $25k of credit to get a discount of 20% and contract for $20k.


## Order Form

An Order Form is a lightweight document that captures the customer details, credit amount, discount, term, and signatures from both 
PostHog and the Customer.  They are either governed by our standard terms or a custom MSA (see below).

You will likely need to use the [Pricing Calculator](https://docs.google.com/spreadsheets/d/1QsDV2ECtMwM9IfC_D7Embmpu7K7q6qbq60t8ARglQaI/edit#gid=358353731) to get the correct credit amount to be included in the order form.

### Creating an Order Form

We use [PandaDoc](https://app.pandadoc.com/a/#/) to handle document generation, routing and signature.  Ask Cameron or Simon for access if you don't have it.

1. The [order form template](https://app.pandadoc.com/a/#/templates/dpuESjnYBeytVREMxLxGuC) to use is titled `[Client.Company] PostHog Cloud Order Form - <MMM YYYY>` 
2. When looking at the template, click the link to **Use this template** in the top bar.
3. In the Add recipients box which pops up:
   1. Replace `<MMM YYYY>` with the month and year the contract starts (e.g. March 2023)
   2. Add the Client email, first and last name 
   3. Add the PostHog Signer email - normally Cameron or Simon
   4. Click continue
4. In the pricing table, set the total amount of credit in the Amount box next to **PostHog Cloud Credit**
5. At the bottom of the pricing table, set the **Discount %** just above the Total
6. On the right of the screen there is a sidebar, select the **Variables** tab and populate them as follows:
   * **Client Address Information** - Needs to be their legal correspondence address (check with your customer contact)
   * **Client.Company** - The legal company name
   * **Contract.Discount** - The discount % (appears in the Additional credit purchase section)
   * **Contract.EffectiveDate**
     - Set the start date of the contract in the format DD MMM YYYY (e.g., 01 Feb 2023). For a new customer, this would be the date they choose to start their subscription. For an existing customer, we have two options:
       - **Immediate Activation:** If the customer wishes to start using the credits immediately, set the start date to the beginning of their current billing period. This backdating ensures that the credits are applied correctly to the current billing cycle.
       - **Next Billing Cycle:** If the customer prefers to begin their annual plan at the start of their next billing cycle, set the start date accordingly. This option aligns the contract start date with the upcoming billing period.
       - For example, let’s say it’s October 15 and you’re setting up an annual plan. You have a pay-as-you-go subscription that started on September 1, and the next billing date is November 1. 
           - If a customer wants to start using credits immediately for the October cycle, your contract start date should be October 1.
           - If a customer wants to start using credits starting the next billing cycle, your contract start date should be November 1.
           - If you set the start date correctly, our Zapier automation flow will create the invoices with correct dates so our revenue calculations are not affected from the transition.
     - **Note:** Pay-as-you-go products are charged after the end of the period, while flat-rate subscriptions are charged at the beginning of the period. As a result the first two payments on a monthly schedule may occur within the same billing period as part of the transition. Make sure to send a note to the customer to ensure they're fully informed!

   * **Contract.Term** - The term in months of the contract (12 months by default)
7. If an MSA is being used rather than the standard terms you will need to replace the following text:
   > PostHog Cloud License Terms appearing at: https://www.posthog.com/terms and Privacy Policy appearing at: /privacy (collectively the “Agreement”)
   
   with
   
   > PostHog Cloud License Terms executed by and between PostHog, Inc. and CUSTOMER LEGAL NAME (the “Agreement”)

8. You should link the order form to the HubSpot deal using the sidebar on the right so that we have a reference to the completed paperwork from our CRM.

### Routing an Order Form for review and signature

1. When viewing the order form, check the recipients tab in the sidebar.  The Client and PostHog roles should be filled in.
2. A signing order should also be set, with the Client signing first (so they can review it before we sign).
3. Ensure Document forwarding and Signature forwarding are set to on so that our Contact can re-assign the document if needed.
4. Click Send at the top of the document and add a message explaining the context of the order form.
5. Once the Client and then PostHog have signed it you should get an email to confirm completion.
6. Don't forget to link to a deal in HubSpot and close the associated deal.
7. Zapier will [automatically add](https://zapier.com/editor/217375860) a record in the [Annual Plan Table](https://tables.zapier.com/app/tables/t/01HGX2N9JXNV2EEDYARD24901R) with the PandaDoc Order Form ID.  See the [Billing](/handbook/growth/sales/billing) page for steps on how to use this and automate the setup of their Stripe billing components.
8. Celebrate!

## Master Services Agreement (MSA)

Occasionally, customers will want to sign an MSA instead of referencing our terms in an order form.  We don't have this templated in PandaDoc yet as it's so infrequent.

1. Download a copy of the [PostHog Cloud MSA](https://docs.google.com/document/d/155w70ZAHecVZcDqTq2_415dvaq2Bk-8QlEOozjq1hG8/edit#heading=h.y38xfjgcg4xm) as a Word Document (legal teams prefer this format) and share it with your Customer contact.
2. They may want to propose changes (also known as 'redlines').  Work with Fraser to get these agreed.
3. Create a new document in PandaDoc, you can choose to either import from Google Drive or upload from your local machine.  This should be the clean, non-redlined document as agreed by both parties.
4. Change the name to be `PostHog Cloud MSA - CUSTOMER LEGAL NAME`.
5. Add the Client and PostHog (fraser@posthog.com) as roles.
6. Add a Signature, Name and Title field for both PostHog and the Customer.
7. Check the signing order (Client, then PostHog normally).
8. Send for signature.

## Business Associate Agreement (BAA)

We offer HIPAA Compliance on PostHog Cloud and as such health companies will require us to sign a Business Associate Agreement with them.  As this means we take on increased financial risk in case of a breach we 
ask them as a minimum to subscribe to the Teams plan which is a guaranteed monthly payment.

1. Ask the customer to subscribe to the Teams plan (as well as any other paid plans they wish to use).
2. Create a new document from the [PandaDoc Template](https://app.pandadoc.com/a/#/templates/4psCXzU527sNE6WEbFBg3a).
3. All you need to do it set the `Client.Company` variable and then send it to them for review and signature.
4. Once the client has signed it then it will get routed to Fraser for countersignature.
5. You'll get a notification when everybody has signed it - _don't forget to update the *BAA Signed Date* property on the HubSpot company record,_ so we can keep track of who we have signed a BAA with.
