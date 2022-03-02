---
description: >-
  This documentation is both an educational and a technical resource. We hope it
  will be equally useful for both technical and non-technical readers.
---

# Getting Started

## I want to learn more about Unstoppable Domains

Unstoppable Domains are decentralized. This makes them, in a word, unstoppable. Once a user claims a domain to a wallet, they have absolute control over that domain. Domains can be transferred, updated, and linked to other services without any involvement from Unstoppable Domains. Unstoppable Domains cannot deactivate, change, or transfer a domain's records without a user's permission.

To learn more about the company, please browse our [general website](https://unstoppabledomains.com), watch the learning materials and videos from our [Youtube Channel](https://www.youtube.com/c/UnstoppableDomains/videos), and listen to our popular, educational [UD Podcast Channel](https://open.spotify.com/show/2ZlyOpkkprGKS5KODk1PSS).

To learn more about how our product works under the hood, see the following pages:

{% content-ref url="domain-registry-essentials/cns-smart-contracts.md" %}
[cns-smart-contracts.md](domain-registry-essentials/cns-smart-contracts.md)
{% endcontent-ref %}

{% content-ref url="domain-registry-essentials/uns-vs-cns-comparison/architecture-overview.md" %}
[architecture-overview.md](domain-registry-essentials/uns-vs-cns-comparison/architecture-overview.md)
{% endcontent-ref %}

{% content-ref url="domain-registry-essentials/uns-smart-contracts.md" %}
[uns-smart-contracts.md](domain-registry-essentials/uns-smart-contracts.md)
{% endcontent-ref %}

{% content-ref url="domain-registry-essentials/uns-vs-cns-comparison/uns-architecture-overview.md" %}
[uns-architecture-overview.md](domain-registry-essentials/uns-vs-cns-comparison/uns-architecture-overview.md)
{% endcontent-ref %}

Also, visit the [List of Integrated Apps](https://unstoppabledomains.com/apps) to draw inspiration from other apps that have successfully integrated Unstoppable Domains.

## I want to add Unstoppable Domains to my app to send and receive crypto

Unstoppable Domains supports 260+ cryptocurrencies. The most common way to integrate with Unstoppable Domains is through [simple domain resolution](domain-registry-essentials/resolving-domain-records.md). This process converts cryptocurrency addresses to a human-readable or user-friendly name. See the guides on [Crypto Payments](send-and-receive-crypto-payments/crypto-payments.md), [Resolution Service API](send-and-receive-crypto-payments/crypto-payments.md#domain-resolution-using-resolution-service), [Resolution Libraries](send-and-receive-crypto-payments/resolution-libraries/), and [Library Configuration](send-and-receive-crypto-payments/resolution-libraries/library-configuration.md) for more detail on integrating UD into your app.

## I want to support Unstoppable Domains in my web browser

Allow your users of your browser to create and view decentralized websites. Individuals control their own content and identity with a decentralized website. The website is **decentralized**, by being created on the Ethereum blockchain, and the domain is stored in a user’s wallet, just like a cryptocurrency. This means that no one can delete content (such as blogs, podcasts, artwork, social media) or move it around other than the domain owner. See the guides on [Resolving Domains in Web Applications](support-unstoppable-domains-in-a-web-browser/resolving-domains-in-web-applications.md) and [Browser Resolution Algorithm](support-unstoppable-domains-in-a-web-browser/browser-resolution-algorithm.md). For a list of test domains, see [Browser Resolution Test Domains](support-unstoppable-domains-in-a-web-browser/test-domains.md).

## I want to allow my users to manage their existing domains

Your app can edit domain metadata manually with a direct connection to the appropriate blockchain. We strongly recommend prior experience with blockchain development before starting this type of integration, so please familiarize yourself with [CNS Smart Contracts](domain-registry-essentials/cns-smart-contracts.md) or [UNS Smart Contracts](domain-registry-essentials/uns-smart-contracts.md) along with [Managing Domain Records](allow-my-users-to-manage-existing-domains/managing-domain-records.md) and [Managing Domain Ownership](allow-my-users-to-manage-existing-domains/managing-domain-ownership/).

Popular open-source crypto wallet, MyEtherWallet, has implemented domain management and can be also used as a reference for implementation: [MyEtherWallet Code Reference](https://github.com/MyEtherWallet/MyEtherWallet/tree/master/src/dapps/Unstoppable) and [MyEtherWallet Website](https://www.myetherwallet.com).

## I want to sell domains to users in my app

If you want to resell domains, you must first [Register as A Reseller](sell-domains-to-users-in-my-app/register-as-reseller.md) with Unstoppable Domains and configure your reseller account to accept [Stripe](sell-domains-to-users-in-my-app/reseller-integration-guides/stripe-payments-guide.md) and/or [CoinBase payments](sell-domains-to-users-in-my-app/reseller-integration-guides/coinbase-payments-guide.md). You may also visit the [Buy Domain: Reseller Demo](https://unstoppabledomains.github.io/reseller-demo/#/reseller-demo) to test out the platform before integration. See the [Reseller API Endpoints](sell-domains-to-users-in-my-app/reseller-api-endpoints.md) for interactive guides and detailed parameters.

## I want to build a decentralized website and link it to my domain

If you are new to IPFS and decentralized websites (d-web), we recommend that you start with the [IPFS Overview](build-a-decentralized-website/overview-of-ipfs-and-d-web.md). After purchasing a domain from UD, you can build your d-website using a [template](build-a-decentralized-website/connecting-your-d-website-to-your-domain/using-a-template-for-your-d-website.md) or [custom design](build-a-decentralized-website/connecting-your-d-website-to-your-domain/building-a-custom-d-website.md). See the guide on [Resolving a D-Website in a Browser](build-a-decentralized-website/resolving-a-d-website-in-a-browser.md) to view your d-website after [connecting it to your domain](build-a-decentralized-website/connecting-your-d-website-to-your-domain/).

## I want to integrate Login with Unstoppable or use the Unstoppable Authorization Server

[Login with Unstoppable](login-with-unstoppable/high-level-overview.md) is a feature that allows any Unstoppable Domain owner to login and share information like _email_ with applications. This allows developers to learn more information about their users without having to host or maintain their own CRM system. With current wallet-based sign-in methods it is difficult or impossible for application developers to contact their users.

Login with Unstoppable is built using the new Unstoppable [Authentication protocol](login-with-unstoppable/authorization-server/authentication-protocol.md) or simply **UAuth**. UAuth is an authorization system built with domains as the primary subject of authorization instead of usernames or wallet addresses. The UAuth protocol is an extension of the OpenID Connect (OIDC) protocol that allows Unstoppable Domain owners to designate authorization servers (OpenID Providers) to authorize access to digital resources a user owns on that user’s behalf. Currently, Login with Unstoppable is configured to share the email address associated with their account on [unstoppabledomains.com](http://unstoppabledomains.com). Future updates will allow users to share other metadata such as social profiles and community memberships with their login, as well as receive direct requests from applications to share specialized information. See the guides on [Domain Owner Configuration](broken-reference), [Getting Login Credentials](login-with-unstoppable/getting-login-credentials.md) and [Login Integration](login-with-unstoppable/login-integration-guides/) to get started.

## I want to support Unstoppable domains on Polygon L2 Network

Unstoppable Domains uses [Polygon](https://polygon.technology) as our Layer 2 (L2) scaling solution. This allows us to make our NFT domains free to claim and manage on L2, and UD customers will no longer have to pay claim fees, renewal fees, or [gas fees](https://youtu.be/h3rP3Ptvka4). Domain minting has already started on Polygon L2 for all Unstoppable domains with future updates planned for domain management and domain transfer (between L1 and L2 or vice versa). See the [Polygon High Level Overview](polygon-l2-network/polygon-high-level-overview.md) for more on the benefits, considerations, and planned releases for Polygon L2. For developers, we have outlined the steps needed to support Unstoppable domains on Polygon L2 in our [Developer Integration Guide](polygon-l2-network/polygon-developer-integration.md).

## I want to promote my UD integration

We offer free advertising for UD integrated apps. Once your app has a working Unstoppable Domains integration, [register it here](https://unstoppabledomains.com/app-submission). Registered apps appear on the Unstoppable Domains [homepage](https://unstoppabledomains.com) and [Applications](https://unstoppabledomains.com/apps) page — putting your app in front of tens of thousands of potential customers per day.

Also, every week we select a newly-integrated app to feature in the Unstoppable Update newsletter. This newsletter is delivered to\~100,000 crypto fanatics — all of whom could become new customers to grow your business.

## I want to get support or connect with other developers

If you have any questions, join our [Discord channel](https://discord.gg/b6ZVxSZ9Hn) for real-time support from us and the community.
