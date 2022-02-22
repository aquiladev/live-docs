---
description: >-
  This guide covers the process for configuring the Reseller account to accept
  Stripe payments. Payout information can be tracked in the UD Reseller
  Dashboard.
---

# Stripe Payments Guide

{% hint style="warning" %}
The Stripe feature has been temporarily disabled. Resellers will be notified when  support for this feature has resumed.
{% endhint %}

Unstoppable Domains supports [Stripe](http://stripe.com) payments. Stripe is a payment provider that allows you to accept credit cards, PayPal, and Apple Pay from customers. This is a recommended and **secure** payment method for resellers that mostly use client side applications.

The following diagram shows the general process that takes place between Stripe and Unstoppable Domains, after a customer buys a domain.

![Payment flow for pre-paid domain purchases, such as Stripe](<../../.gitbook/assets/Paid domains claiming - Prepayment.png>)

## Step 1: Create a Stripe Account

You must [Create a Stripe Account](https://dashboard.stripe.com/register?redirect=%2Fsettings%2Faccount%2F) in advance before you connect it to your Unstoppable Domains reseller account.

## Step 2: Connect Stripe to Unstoppable Domains

There is a stripe connect button in the [UD Reseller Dashboard](https://unstoppabledomains.com/resellers) for live and test connections. At UD, we use a different stripe API key for live and test orders. These Stripe API keys are public keys and they are safe to reveal.

* pk\_test\_\* (reseller-test-\* namespace)
* pk\_live\_\* (all other domains)

The **Stripe Live Connect Button** is how you get paid by Unstoppable Domains when your customers make a purchase; it uses real money and generates real transactions. The **Stripe Test Connect Button** does not involve real money and uses test credentials to integrate.

![Strive Live and Stripe Test payment setup areas](../../../.gitbook/assets/screen-shot-2021-07-12-at-2.04.09-pm.png)

![](../../../.gitbook/assets/8.png)![](../../../.gitbook/assets/9.png)

After clicking the Stripe Live or Stripe Test **Connect Button**, you will be walked through the Stripe Integrations form.

![Stripe integrations form to connect your Stripe and UD accounts](../../../.gitbook/assets/10.png)

Once your Stripe and Unstoppable Domains accounts have been connected, your Stripe API key will appear directly in your Stripe Dashboard.

### Other Stripe Considerations

To begin accepting payments from your customers, Stripe requires you to embed their form into your application or website. Please see the documentation for [Accepting Payments using Stripe](https://stripe.com/docs/payments/accept-a-payment?platform=web) for more information.

Stripe generates a token ID for each transaction, which is later used by UD to process the ‘Buy Domain’ API endpoint. This keeps Unstoppable Domains from needing to store your customer’s sensitive data. Please see the documentation for [Accepting Payments using Stripe Elements](https://stripe.com/docs/payments/accept-a-payment-charges#web) for more information.

## Step 3: Receive Stripe Payouts

Stripe payouts occur daily directly from Stripe and can be tracked within the reseller dashboard by clicking on the “View Test Dashboard” or “View Live Dashboard” button depending on which payouts are being tracked.

![Button selection for tracking Stripe payouts](../../../.gitbook/assets/screen-shot-2021-07-12-at-2.53.26-pm.png)

{% hint style="info" %}
The **View Live Dashboard** and **View Test Dashboard** buttons will only appear after the Stripe Live or Stripe Test options are successfully connected, linking your Stripe and UD Reseller Accounts.
{% endhint %}

### Stripe Payouts Tab

Clicking either of the “View Dashboard” buttons displays the main tab of the payouts screen, which lists all transactions with dates and payment amounts. The figure below shows the main view of the Payouts screen.

![Main/default view of Stripe Payouts (i.e., payouts tab) ](../../../.gitbook/assets/24.png)

### Stripe Accounts Tab

Click the ‘Account’ tab to view Stripe account information or to update your Stripe banking information.

![View of Stripe Account information (i.e., account tab)](../../../.gitbook/assets/25.png)



{% hint style="success" %}
**Congratulations!** You just setup your Reseller account to accept Stripe payments.
{% endhint %}
