# Document M365 Users Setup

{% hint style="danger" %}
Note that this documentation applies to the v2 of this crate.

The original crate documented against an asset called "M365 Users (auto)", the new version uses "MS365 Users (auto)" instead.

It is recommended that you disable the trigger on the old automations and delete the flexible asset types to avoid confusion.
{% endhint %}

## Introduction

The "Document M365 User Information" crate is a handy automation tool designed to streamline the documentation of user information in Microsoft 365. It records details such as licences, aliases, full access, send as access, and standard attributes like password changes, directory synced statuses, and more.

The purpose of this crate is to automate the process of user management, auditing, reporting, and overall IT administration. The automation benefits include improved reporting accuracy, time-saving through automated documentation, and easy troubleshooting with readily available user information. Out of date documentation provided little benefit, so this ensures that automated documentation is constantly dynamically updated.

Before using this automation, ensure you have an existing Microsoft 365 account and your ITGlue or Hudu integration is set up.

## What Does the Automation Do?

The automation fetches user details from the Microsoft 365 API, as well as the Exchange integration, and documents this information on your ITGlue platform. The automation also links the M365 user to the Contact Record in ITG for easier tagging and access.

The benefits include:

* Automated documentation saving you considerable time.
* Enhanced internal reporting and auditing with systematically documented user information.
* Easy troubleshooting due to readily available user data.

## Compatibility

This automation is compatible with ITGlue at the moment, and we are actively working on integrating it with Hudu.

If your system or platform is not on this list, please let us know. We'll explore whether it can integrate with our crate.

## Automation Steps

1. The automation fetches user details from various integrations such as MS Graph and Exchange Online.
2. The information is combined into a single JSON object containing all the information about that user, including group names etc.
3. The information is then updated, or creates a new flexible asset and uses a HTML table to insert the information in a nice-to-look-at way.
4. The user is then related to the contact record.

## Getting Started

**Step 1:** Ensure that you have the Microsoft Graph, Exchange Online and ITG integrations set up and configured, which you can get to via the below links

[Microsoft Graph](https://app.rewst.io/integrations/microsoft\_graph)

[Microsoft Exchange Online](https://app.rewst.io/integrations/microsoft\_exo)

[ITGlue](https://app.rewst.io/integrations/it\_glue)

**Step 2:** Unpack the crate in the marketplace. Find the crate titled "Document M365 User Details V2". You can also [find the crate by clicking here](https://app.rewst.io/marketplace/crates/ad23cb3a-d4fb-4066-91d1-719ea95a6355)

## Feedback

Genuinely, if you like this crate and have followed these instructions to get it up and running, we'd love to hear from you! We're always looking for feedback on how we can improve our crates, so please [click me](mailto:roc@rewst.io) and let us know what you think! If you'd like to only say thanks, that's cool too! You can [click me instead](https://engine.rewst.io/webhooks/custom/trigger/db81c9a8-13f7-458a-9306-287054605844/c47fdd7f-4075-47a8-ba92-94e790e67c06?crate=DocumentUsers) and we'll send an awesome gif to our internal slack channel! 😁
