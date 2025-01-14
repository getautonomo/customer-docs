# Zapier

You can connect Tonomo to any of the [5,000+](https://zapier.com/apps) apps from Zapier. Because we connect via Webhooks, it does require at least having the [Starter ](https://zapier.com/pricing)plan.

A "Webhook" is a piece of code that triggers when something happens in Tonomo. Currently, when an order is created or the status changes, we trigger the Webhook to send information about the order to Zapier. Then you can program Zapier to send that information to another app.

## 1) Connect your App

If you haven't already, connect the app you want to integrate with Tonomo to Zapier. [https://zapier.com/app/connections](https://zapier.com/app/connections)

![](<../../.gitbook/assets/image (151).png>)

This just requires clicking **+ Add Connection** and logging into your app.

## 2) Set Trigger

Click the big orange **Create Zap** button on the left of your screen.

From the Trigger page, search for and select **Webhooks by Zapier**

![](<../../.gitbook/assets/image (173).png>)

In the Event field, click **Catch Hook** and **Continue**

![](<../../.gitbook/assets/image (159).png>)

This will generate a Webhook URL. Click **Copy**. This will be placed in one of a few places depending on the action you're trying to perform. So check below for some example workflows.

![](<../../.gitbook/assets/image (48).png>)

## 3) Set Action

### Send Customer Information to Email Platform

{% hint style="info" %}
This webhook is useful for if you want to send customer information to an app like mailchimp every time someone orders. This way Mailchimp can update audiences and send welcome emails.
{% endhint %}

Enter the webhook at the bottom of **Configure Booking** > **General** under the **Booking Created Webhook** and click **Save.**

![](<../../.gitbook/assets/image (161).png>)

To test, create an order with dummy customer contact information (Don't just leave stuff blank, create an order as if it was real). Jump back into Zapier and click **Test Trigger.** The test order can take up to a couple minutes to come through, so give it a few tries.\
\
If it's successful, move on! If it's not, double check your URL you pasted to Tonomo matches the one Zapier provided. Then reach out to your support person if the issue persists.

From the next window in Zapier, select the app you want to connect to. In our case, Mailchimp.

![](<../../.gitbook/assets/image (130).png>)

Select an event you want to trigger. In our case, I want to add a user to a specific mail list every time an order is created.&#x20;

![](<../../.gitbook/assets/image (34).png>)

The final step is telling Mailchimp what I want to happen with the new contact information. I can add it to a specific Audience, change tags, add them to a group, etc.

![](<../../.gitbook/assets/image (11) (1).png>)

### Send Post-Order Follow up Emails

{% hint style="info" %}
This method is useful if you want to follow up with customers after a few days to ask for feedback.
{% endhint %}

Complete Steps 1 and 2 above. When you generate the webhook, enter it into the Booking complete Webhook at the bottom of **Configure Booking** > **General** and click **Save**.

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If you set an order to Complete multiple times, the webhook will fire multiple times and therefore send multiple emails!
{% endhint %}

The first app we want to add is a delay. Click the **+** symbol and then search for **Delay by Zapier.** Click the top result.&#x20;

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Click **Delay For**.

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

Enter the length of the delay. I put 2 days for example:

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

Click Continue and now we need to build the email that we want to send. Click the **+** symbol and search for Gmail and add it with the Event type as **Send Email**.

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

Next, we need to set the following fields:\
**To:** search "Email" in the Zapier fields and add the customers email address\
**BCC**: It's common to want a BCC of emails sent, so you can just enter whatever email address at your company you want a copy to go to.\
**From:** Select whichever of the accounts you have connected you want it to come from\
**From Name:** Enter the name of your company or person you want the email to come from\
**Subject:** Enter a combination of plain text and variables to build the subject you want. For example, you might enter "how did" and then enter the variable for the address and ask "go?" at the end. So your subject line would be "How did 1234 main st, Portland, OR go?"\
**Body:** Enter the body of the email in the voice of your company. For example, ask for a review to be placed online or to call you with any issues.

Once all fields have been entered, click **Continue** at the bottom and test.
