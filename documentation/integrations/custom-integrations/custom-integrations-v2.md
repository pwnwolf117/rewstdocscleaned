# Custom Integrations (v2)

## How to Add a Custom Integration in Rewst

This guide will walk you through the steps to add a custom integration in Rewst.

## Steps

Click on `Configuration` -> `Integrations`.

<figure><img src="../../../.gitbook/assets/custom-integrations-step2.png" alt=""><figcaption></figcaption></figure>

Click on `Add New Integration`.

* &#x20;Click on `New Integration` to build your integration from the beginning.
* Alternatively, click on `Add OpenAPI Integration` if you have a JSON file that follows the OpenAPI (or Swagger) specification.

<figure><img src="../../../.gitbook/assets/custom-integrations-step4.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note that Rewst will automatically convert Swagger to OpenAPI if necessary and validate the API specification using the vacuum linting tool. Currently, only JSON files are accepted (not YAML).
{% endhint %}

Click on `Submit`. Once you upload your file and there are no validation errors, you can start configuring your integration.

<figure><img src="../../../.gitbook/assets/custom-integrations-step5.png" alt=""><figcaption></figcaption></figure>

Specify your Configuration details, then click on `Next`.&#x20;

Add a name for your integration, a logo (SVG only), and a description.

<figure><img src="../../../.gitbook/assets/custom-integrations-step6.png" alt=""><figcaption></figcaption></figure>

Choose your authentication method, then click on `Next.`

Add the hostname without "https://", and select an authentication method. Rewst supports:

* API Key
* Basic Auth
* OAuth 2.0 (Authorization code, Client Credentials, or no grant type)
* No Auth

![Choose your authentication method, then click on Next](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/c317aa59-3ed0-416e-8f8b-a402dc21e454/856e953b-9f8f-47f7-9832-edb1448511b6.png?mark-x=1297\&mark-y=573\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz03MiZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

Fill out the authentication defaults, then click on `Next`

Depending on the auth method you chose, you will be presented with a form to fill out the details of the integrations authentication.

![Fill out the authentication defaults, then click on Next](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/75a6b465-2fbd-434a-8bd2-a3f3defe59a0/4f3b3809-7b3e-4ac4-879b-3e3b15b6ee6e.png?mark-x=1287\&mark-y=860\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz03MiZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

Select a pagination method, then click on `Next`

Select from:

* No pagination
* Index
* Page
* Link
* Pointer

![Select a pagination method, then click on Next](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/e49e93e5-2f4f-4f09-b90f-bda1061af815/c9d2b711-107c-4ca6-981f-f14082ce3d36.png?mark-x=1297\&mark-y=499\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz03MiZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

Fill out the pagination details, then click on `Next`

Depending on the pagination method you chose, you will be presented with a form to fill out the details of the integrations pagination.

![Fill out the pagination details, then click on Next](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/a59415ed-02e2-49d5-890f-7c0c6a570890/29d7b649-5ae7-43c1-9b66-d6f49c5cbfbc.png?mark-x=1297\&mark-y=449\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz03MiZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

Edit your actions, then click on `Finalize`

On this step you will create, update, or delete the actions and their parameters

![Edit your actions, then click on Finalize](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/25803396-9f4e-4427-95eb-09ce97998dfa/5aba5597-e73f-477f-a9f7-65bbb166f3f6.png?mark-x=1385\&mark-y=888\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz05MyZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

Click on `Finalize` again.

![Click on Finalize](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/ed9090e3-8b17-4f0d-8b7b-843f52c32c45/9c5a32b7-0ee4-4510-a53a-7af43aea21e6.png?mark-x=950\&mark-y=520\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz05MyZoPTQ1JmZpdD1jcm9wJmNvcm5lci1yYWRpdXM9MTA%3D)

(Optional) Update the status of your integration.

Select one of:

* Draft- The integration is not finalized, can be still be edited, but not installed. Once an integration is finalized it can't be put back in to draft mode.
* Published - The integration will be installable by your organizations and all sub organizations.
* Hidden - The integration is NOT installable by your organizations and all sub organizations, but can be edited.

![(Optional) Update the status of your integration.](https://images.tango.us/workflows/7bbe9055-9c43-4e0d-9aa1-bee39c08cbb8/steps/fad46f6f-526e-4508-8ef7-a16319b615e7/74ef4c73-39b7-4105-a042-240ea5e150bc.png?mark-x=1161\&mark-y=348\&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTMlMkNGRjc0NDImdz0yMDgmaD00NCZmaXQ9Y3JvcCZjb3JuZXItcmFkaXVzPTEw)

\
