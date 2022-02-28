---
description: >-
  This guide covers the process for configuring the Reseller account to claim
  free domains.
---

# Claim Free Domains Guide

Unstoppable Domains offers free domain claiming to Resellers. The free domain claiming criteria will vary based on the Reseller, but when enabled, it allows Resellers to use the following [Reseller API endpoints](../reseller-api-endpoints.md): free domain suggestions, free domain claiming, and reserve free domain.&#x20;

The following diagram shows the general process that takes place between the Reseller and Unstoppable Domains during the free domain claiming process.

![Success flow for claiming free domains with UD](<../../.gitbook/assets/Free domain claiming - Success flow.png>)

## Step 1: Retrieve the Secret Key for Authentication

A secret key is required when a domain is purchased using the **Payback** or **Free** payment type. The secret key should be saved and can only be used on the server-side. This process hasn't been automated yet, so resellers must email [bd@unstoppabledomains.com](mailto:bd@unstoppabledomains.com) to request the secret key.

![Location of Reseller API Token when enabled in the Reseller Dashboard](../../.gitbook/assets/reseller-api-secret.png)

## Step 2: Setup Criteria for Free Domains

* Resellers work with UD administration to establish the "allowed free TLDs" and "allowed free tiers" for the reseller account. **The free domain criteria will vary based on the Reseller.**
* This list of "allowed free TLDs" and "allowed free tiers" is then assigned to the resellers account.&#x20;
* Resellers can only mint a free domain if it matches the tier and has an appropriate TLD.

The table below shows how the pricing tiers are structured at UD. Most free domains will be a Tier 7 or Tier 8 domain with a combination of letters and numbers.

![Pricing tiers for UD domains](../../.gitbook/assets/domain-pricing-tiers.png)

{% hint style="info" %}
Domains containing numerals in the name (i.e: tim1, monica95, etc) are discounted by up to 75% of the standard prices, and most free domains fall within this category.
{% endhint %}

## Step 3: Use the Free Domain Claiming endpoint

The free domain claiming endpoint allows the partner (Reseller ID) to mint free domains for a specified wallet address, if the Reseller is eligible to offer free domains.

The free domain claiming endpoint is implemented as an additional payment type within the [orders API endpoint](../reseller-api-endpoints.md).&#x20;

{% hint style="info" %}
No additional configuration is necessary from the Reseller to begin using this endpoint once the free domains criteria has been established with UD administrators and added to the Reseller account.
{% endhint %}

## Considerations

The following considerations apply to the free domain claiming:

* The Reseller ID will be allowed to provide specified TLD's for free.
* If the Reseller ID doesn't have allowance to provide free domains, then users will not be permitted to claim free domains.
* If the wallet or email already has a free domain, then a second free domain is not permitted.

{% hint style="success" %}
**Congratulations!** You just configured your Reseller account to claim free domains.
{% endhint %}
