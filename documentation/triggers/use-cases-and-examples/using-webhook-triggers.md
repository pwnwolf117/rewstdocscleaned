# Using Webhook Triggers

## Introduction

Webhook triggers are an effective way to kick off a workflow with context from external systems. By sending an API request to a webhook trigger, Rewst will fire the workflow and include any data and/or queries included in the request.

***

## Getting Started with Trigger Setup

### **Navigate to Workflow Creation**

* Go to [Rewst](https://app.rewst.io).
* Select `Workflows` > `Create`.
* Enter a workflow name, like `My First Webhook Trigger`.
* Click `Submit` to proceed to a blank workflow creation screen.
* Add a single [no-op](../../workflows/actions-in-rewst/core-actions.md#no-operation-noop) action to the canvas, name it `BEGIN` and then click `Publish` to save your workflow. (No other actions are needed, as we will just be working with triggers.)

### **Accessing Trigger Configuration**

Click the lightning bolt icon at the top to `Add Trigger`.

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

### **Creating up the Trigger**

* Name & Enable your trigger.
* Choose the trigger type `Core - Webhook`

### **Setting Trigger Parameters**

The following parameters are available for editing:

* Allowed Methods
    * Used to define which HTTP request method is accepted by the trigger. Attempting to send a request with a method not in this list will result in an error
* Include Raw Body
    * Whether to include the raw string sent in the request body in the results as `raw_body`
* Response Body
    * Content to return in response body. {{ REQUEST }} may be used to access request data.
* Response Headers
    * HTTP headers to include in response. {{ REQUEST }} may be used to access request data.
    * **TIP:** Set your content type here if returning a specific format of data, such as `text\html`
* Response Status
    * HTTP status to return in response. {{ REQUEST }} may be used to access request data.
* Secret Key
    * Required to Wait For Results. This value must be included in the header as x-rewst-secret when making calls to this webhook. You will receive a 401 if this field is filled out and the secret key is not provided when making the request. Secrets can be defined in the Organization Variables section of the UI
* Wait for Results
    * If true, calls to the trigger endpoint will redirect to a results endpoint that will return the output of the workflow.

***

### **Accessing Data in a Webhook Trigger Request**

When a Webhook receives a request, it will include data received in the following schema:

```json
{
    body:{},
    headers:{},
    method:"",
    params:{},
    timestamp:""
}
```

Data can then be pulled from this as context variables. For example, to access the value for "test" sent to the webhook as:

```json
{
    "test": "Hello, World!"
}
```

The value can be accessed at `{{ CTX.body.test }}`.

Similarly, if a URL parameter is sent as `?test=Hello`, this can be accessed at `{{ CTX.params.test }}`

***

### **Anatomy of a Webhook URL**

Webhook URLs are formatted consistently using the triggger ID and organization ID. The format is as follows:
`https://engine.rewst.io/webhooks/custom/trigger/{{ Trigger ID }}/{{ Organization ID }}`

Using this information, you can craft webhook links on the fly for organizations a webhook trigger is enabled for. This may be useful for invoking certain workflows using links in a PSA ticket note or email, for example