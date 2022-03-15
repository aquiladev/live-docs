---
description: >-
  This guide covers the process for configuring the Login UI to obtain user
  information and display the authenticated user's domain name instead of
  address.
---

# Login UI Configuration

## Step 1: Access User Information

Authorizations are stored inside `localStorage`, so any identically configured UAuth instance has access to the same users.&#x20;

* If you integrate with the [@uauth/web3-react](https://github.com/uauth/web3-react) or any other solution that uses [@uauth/js](https://github.com/uauth/js) under the hood ([@uauth/bnc-onboard](https://github.com/uauth/bnc-onboard), [@uauth/web3modal](https://github.com/uauth/web3modal)), then you can access the user information by instantiating a separate [@uauth/js](https://github.com/uauth/js) class and calling the `user()` function.&#x20;
* There are also methods on [@uauth/web3-react](https://github.com/uauth/web3-react), [@uauth/web3modal](https://github.com/uauth/web3modal) & [@uauth/bnc-onboard](https://github.com/uauth/bnc-onboard) for getting a UAuth instance on the front end as well.&#x20;

You can use the access methods below to obtain the user information. Retrieving this information will display the domain instead of the wallet address and serves as another confirmation for the user that they have logged in successfully.&#x20;

{% hint style="info" %}
The @uauth.js code snippet below can be used for [Login with Popup](login-integration-guides/login-with-popup.md) and [Login without Popup](login-integration-guides/login-without-popup.md) integrations.
{% endhint %}

{% tabs %}
{% tab title="@uauth.js" %}
```javascript
import UAuth from '@uauth/js'

const uauth = new UAuth({
  // ... options
})

uauth.user()
  .then((user) => {
    // user exists
    console.log("User information:", user)
  })
  .catch(() => {
    // user does not exist
  })
```
{% endtab %}

{% tab title="BNC Onboard" %}
```javascript
// Gets the local UAuth instance.
public get uauth(): UAuth

const uauthBNCOnboard = new UAuthBNCOnboard()

uauthBNCOnboard.uauth.user().then().catch()
```
{% endtab %}

{% tab title="Web3 React" %}
```javascript
public get uauth(): UAuth

const uauthConnector = new UAuthConnector()

uauthConnector.uauth.user().then().catch()
```
{% endtab %}

{% tab title="Web3 Modal" %}
```javascript
const uauthOptions = {
  clientID: "",
  clientSecret: "",
  redirectUri: ""
}

const web3ModalOptions = {
  'custom-uauth': {
    ...uauthOptions}
}

const web3Modal = new Web3Modal(web3ModalOptions)

new UAuth(uauthOptions).user().then().catch()
```
{% endtab %}
{% endtabs %}

Once a user has successfully authenticated, the application should display the user’s domain name in the application’s UI to confirm the authorization was successful. In other words, the UI must show the user’s domain instead of the address.

![UI Example for displaying authenticated user](<../.gitbook/assets/second-UI-example-login-domains (1).png>)

## Step 2: Verify the Login Flow and Scopes

Before launching your application, you should verify the login flow that users will experience and ensure that proper scopes are showing or enabled for users. In the last modal screen shown below, only the minimum scopes are being requested by the application: [openID](scopes-for-login.md#openid-scope), [wallet](scopes-for-login.md#wallet-scope), and [email](scopes-for-login.md#email-scope).&#x20;

{% hint style="info" %}
You must adjust the configuration in the [Login Client](login-client-configuration.md#scopes) to add or remove scopes, such as [humanity\_check](scopes-for-login.md#humanity\_check-scope).
{% endhint %}

![1) User Clicks Login with Unstoppable button to get started](../../.gitbook/assets/login-domains-modal1.png) ![2) User Enters Unstoppable Domain Address to Login to dApp](../.gitbook/assets/login-domains-modal2-v2.png) ![3) User Consent screen details the scopes being requested by dApp](../.gitbook/assets/consent-screen-marked-v2.png)

The modals are further described below:

* **Modal 1.** User clicks on Login with Unstoppable Button.
* **Modal 2.** A modal is displayed which allows the user to begin the authorization process by entering their Unstoppable domain address.
* **Modal 3.** During login, the user will see the resolved address and the information being requested by the application (i.e. the scopes). User must sign the transaction using their wallet address in order to share their information with the dApp.

## Step 3: Download UD Buttons (Node js Only)

For Node.js integrations, the UI or modals being built will require official UD buttons. The table below provides Login with Unstoppable button status and states, which can be downloaded for use in custom Node.js integrations.

| Status  | Small                                       | Large                                         |
| ------- | ------------------------------------------- | --------------------------------------------- |
| Default | ![](../../.gitbook/assets/default-icon.png) | ![](../../.gitbook/assets/default-button.png) |
| Hover   | ![](../../.gitbook/assets/hover-icon.png)   | ![](../../.gitbook/assets/hover-button.png)   |
| Pressed | ![](../../.gitbook/assets/pressed-icon.png) | ![](../../.gitbook/assets/pressed-button.png) |

{% hint style="success" %}
**Congratulations!** You just configured the Login with Unstoppable UI.
{% endhint %}
