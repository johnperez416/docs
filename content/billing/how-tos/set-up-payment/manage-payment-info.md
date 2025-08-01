---
title: Managing your payment and billing information
intro: 'Learn how to manage your payment information and history, and update your billing contacts using the new billing platform.'
versions:
  feature: enhanced-billing-platform
redirect_from:
  - /billing/using-the-enhanced-billing-platform-for-enterprises/managing-your-payment-and-billing-information
  - /billing/using-the-billing-platform/adding-or-editing-a-payment-method
  - /billing/using-the-billing-platform/viewing-your-payment-history-and-receipts
  - /billing/using-the-billing-platform/adding-information-to-your-receipts
  - /billing/using-the-billing-platform/setting-your-billing-email
  - /billing/using-the-new-billing-platform/managing-your-payment-and-billing-information
  - /billing/managing-your-github-billing-settings/adding-or-editing-a-payment-method
  - /billing/managing-your-github-billing-settings/adding-information-to-your-receipts
  - /billing/managing-your-github-billing-settings/setting-your-billing-email
  - /billing/managing-your-github-billing-settings/viewing-your-payment-history-and-receipts
  - /billing/managing-your-billing/managing-your-payment-and-billing-information
topics:
  - Billing
  - Enterprise
  - Team
  - Receipts
permissions: '{% data reusables.permissions.enhanced-billing-platform %}'
product: '{% data reusables.billing.enhanced-billing-platform-product %}'
shortTitle: Manage payment info
contentType: how-tos
---

You can view your payment information and history, and update your billing contacts.

## Supported payment methods

These are the supported payment methods for metered billing:

* Invoice – Managed accounts only
* Credit card – Unmanaged accounts, or as a nonrecurring method for managed accounts
* PayPal – Unmanaged accounts, or as a nonrecurring method for managed accounts
* Azure Subscription ID – Not available for personal accounts
* Automated Clearing House (ACH) – Managed accounts only

Accounts with volume licenses and metered billing can use multiple payment methods.

* For unmanaged accounts, you might pay for volume licenses with a credit card or PayPal, and metered usage with an Azure Subscription ID.
* For managed accounts, you might pay for volume licenses via invoice, and metered usage via Azure Subscription ID.

{% data variables.product.prodname_copilot_short %} standalone accounts, which traditionally used Azure Subscription IDs, can now also pay by credit card. Contact your {% data variables.product.github %} representative for details.

{% ifversion fpt %}

## Connecting your Azure subscription

You must know your Azure subscription ID. For more information, see the following documentation or [contact Azure support](https://azure.microsoft.com/support/).

* [AUTOTITLE](/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription)
* [Get subscription and tenant IDs in the Azure portal](https://learn.microsoft.com/en-us/azure/azure-portal/get-subscription-tenant-id) in the Microsoft Docs

{% elsif ghec %}

## Prerequisites for paying through Azure

* You must be new to {% data variables.product.prodname_ghe_cloud %} to begin with usage-based billing through an Azure subscription. If your company already uses {% data variables.product.github %}, you can use {% data variables.product.prodname_importer_proper_name %} to migrate your resources to a new subscription that bills through Azure. For more information, see [AUTOTITLE](/migrations/using-github-enterprise-importer/understanding-github-enterprise-importer/about-github-enterprise-importer).
* Prepaid usage is not currently available for usage-based billing through Azure.
* You must know your Azure subscription ID. For more information, see the following documentation or [contact Azure support](https://azure.microsoft.com/support/).

  * [AUTOTITLE](/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription)
  * [Get subscription and tenant IDs in the Azure portal](https://learn.microsoft.com/en-us/azure/azure-portal/get-subscription-tenant-id) in the Microsoft Docs

## Connecting your Azure subscription

After creation of your new enterprise on {% data variables.product.prodname_dotcom_the_website %}, to begin usage-based billing through Azure, you must connect your Azure subscription.

> [!IMPORTANT] If you don't use {% data variables.product.prodname_emus %}, connection of an Azure subscription will immediately end your trial and begin paid usage.

For more information, see [AUTOTITLE](/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription#connecting-your-azure-subscription-to-your-enterprise-account).

## What does my Azure invoice look like?

After you connect your Azure subscription, usage for {% data variables.product.company_short %}'s products will appear on your Azure invoice, summarized by product family.

For example, if you use this billing arrangement for {% data variables.product.prodname_ghe_cloud %} and {% data variables.product.prodname_GHAS %}, usage and price excluding tax for each line item will appear as follows.

| Product Family Usage Charges | Total (excluding Tax) |
| :- | :- |
| GH ENTERPRISE | AMOUNT |
| GH ADVANCED SECURITY | AMOUNT |

For more information about your Azure invoice, see [Understand terms on your Microsoft Azure invoice](https://learn.microsoft.com/azure/cost-management-billing/understand/understand-invoice) in the Microsoft Docs.

The {% data variables.product.company_short %} products on your Azure invoice are also MACC-eligible. For more information, see [Track your Microsoft Azure Consumption Commitment (MACC)](https://learn.microsoft.com/azure/cost-management-billing/manage/track-consumption-commitment) in the Microsoft Docs.

{% endif %}

## Managing payment information

{% ifversion fpt %}

You can view and edit your billing information and update your payment method.

1. In the upper-right corner of any page on {% data variables.product.prodname_dotcom %}, click your profile picture.

   * For **personal accounts**, click **Settings**, then in the **Access** section of the sidebar, click **{% octicon "credit-card" aria-hidden="true" aria-label="credit-card" %} Billing & Licensing**.
   * For **organizations**, click **Your organizations**, then next to the organization, click **Settings**. In the organization sidebar, click **{% octicon "credit-card" aria-hidden="true" aria-label="credit-card" %} Billing & Licensing**.

{% elsif ghec %}

You can view and edit your billing information, update your payment method, and view active coupons.

>[!NOTE] This does not apply to invoiced enterprise accounts.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.billing.enterprise-billing-menu %}

{% endif %}

1. Click **Payment information**.
1. Click **Edit** to edit your payment information or **Remove** to delete your payment method.
1. Follow the prompts.

>[!NOTE] You may see an authorization hold on your provided payment method once its updated or after accruing significant usage of metered services. Authorization holds are temporary and are released as quickly as possible.

## Troubleshooting payment method issues

If you encounter issues when adding or updating your payment method, you can try the following:

1. Retry adding your payment method.
1. Try adding a new payment method.
1. Reach out to {% data variables.contact.github_support %} or your customer representative for additional assistance.

## Viewing payment history

You can view your payment history, including the date, amount, and payment method. You can also download past payments.

1. Display the **Billing and Licensing** {% ifversion fpt %}section of the sidebar of the organization settings{% else %}page for the enterprise{% endif %}.
1. Click **Payment history**.

## Managing billing contacts

You can add an email address to receive billing notifications regarding payments and budget threshold alerts.

{% ifversion fpt %}

1. Display the **Billing and Licensing** section of the sidebar of the organization settings.
1. Click **Additional billing details**.
1. In the table of "Email recipients":
   * Click **Add** and follow the prompt to add a new billing contact.
   * Use the **Edit** drop-down for a contact to either remove the contact or make that contact the primary billing contact.

{% else %}

1. Display the **Billing and Licensing** page for the enterprise.
1. Click **Billing contacts**.
1. Click **Add** in the upper-right corner and follow the prompt.
1. Click {% octicon "pencil" aria-label="The edit icon" %} to edit the primary billing contact or {% octicon "kebab-horizontal" aria-label="Show options" %} to either remove a contact or make a contact the primary billing contact.

{% endif %}
