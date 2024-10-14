---
description: >-
  Simplify Your Microsoft Service Integrations bringing together your Microsoft
  Graph, Exchange Online, CSP, and Azure integrations into one streamlined
  setup.
---

# Microsoft Cloud Integration Bundle

***

## Overview

Welcome to the Rewst Microsoft Cloud Integration Bundle guide. This document is designed to assist you in setting up and managing integrations with Microsoft services like Microsoft Graph, Exchange Online, CSP, and Azure. Whether you are transitioning from the Legacy Rewst App or starting anew, this guide will provide you with all the necessary steps to ensure a smooth integration process within your Microsoft tenant.

## Key Benefits

* **Granular Permission Control:** Customize permissions tailored to your organization’s needs.
* **Simplified Management:** Centralize the management of all Microsoft integrations through the Rewst platform.
* **Enhanced Security:** Benefit from advanced security measures protecting your data.
* **Future-Proof:** Keep your integrations current with continuous updates and enhancements.

***

## Getting Started with the Bundle

***

### **Initial Setup**

1. **Login**: Access your Rewst account by navigating to the Rewst platform and logging in with your credentials.
2. **Navigate to Integration Setup**: Once logged in, proceed to the dashboard, and under Configuration -> Integrations, locate the Microsoft Cloud Integration Bundle.
3. **Follow the Configuration Steps:** Select Integrations -> Configuration Parameters -> Tenant Permissions -> Authorize Integrations

***

### Step 1: Select Integrations

* **Microsoft Graph:** Enables automation of M365 services. Utilize the Microsoft Graph API to integrate M365, Entra ID, SharePoint, OneDrive, Teams, etc., into Rewst workflows.
* **Microsoft Exchange Online:** Facilitates automation of email and collaboration management. Access and manage mailboxes, distribution groups, and more through the Microsoft Exchange Online API within your Rewst workflows.
* **Microsoft CSP:** Aids in cloud service provider management. Through the Microsoft Partner Center API you can create & manage organizations within Rewst and provide delegated access.
* **Microsoft Azure:** Automates cloud infrastructure management. Create, read, update, and delete Azure resources using the Microsoft Azure API within Rewst workflows.

***

### Step 2: Configuration Parameters

Configure the Microsoft Entra App Registration that Rewst will use to interact with your Microsoft tenant. Options include:

* **Rewst Microsoft Cloud Connector:** Uses the Rewst Cloud Connector, which features dynamic permission management. Recommended for users seeking a quick & easy integration process.
* **Owned App Registration:** Use an App Registration created and managed by you within your Microsoft tenant. This is suitable for users who require or prefer maximum customization.
* **Legacy Rewst App (Deprecated):** The legacy Rewst App Registration that has a static set of permissions. This option is being deprecated in favour of our new bundle integration.

{% hint style="success" %}
See more about bringing your own app on the [owned-app-registration.md](owned-app-registration.md "mention") page.
{% endhint %}

{% hint style="warning" %}
Customers wanting more information on how to migrate from the legacy app can review the [migrating-legacy-microsoft-integrations.md](migrating-legacy-microsoft-integrations.md "mention") page.
{% endhint %}

***

### Step 3: Tenant Permissions&#x20;

Review each of the integrations respective pages for the individual details on tenant details and permissions:

* [**Microsoft Graph**](microsoft-graph/microsoft-graph-integration-setup.md)&#x20;
* [**Microsoft Exchange Online**](microsoft-exchange-online/microsoft-exchange-online.md)
* [**Microsoft CSP**](microsoft-csp/microsoft-csp-integration-setup.md)
* [**Microsoft Azure**](microsoft-azure/microsoft-azure-integration-setup.md)

***

### **Step 4: Authorize Integration**

* In the `Authorize Integrations` section, click the `Authorize` button. This will open a Microsoft login window for authentication.
* Follow the prompts to complete the authorization process.

***

## **Troubleshooting Tips**

* **Authorization Issues**: If you encounter problems during the authorization step, ensure that you are using the correct account and that all permissions are properly set.
* **Permission Configuration Errors**: Double-check the permissions if there are issues with accessing certain functionalities. Ensure that the appropriate permissions are enabled and correctly configured.

{% hint style="info" %}
For troubleshooting tips, check out the [troubleshooting-installation-issues.md](common-issues-with-microsoft-bundle/troubleshooting-installation-issues.md "mention") and [common-issues-with-microsoft-bundle](common-issues-with-microsoft-bundle/ "mention") pages.
{% endhint %}

## **Best Practices for Microsoft Integrations**

For best practice information please refer to: [Best Practices for Microsoft Integrations](https://docs.rewst.help/documentation/integrations/cloud/authorization-best-practices).
