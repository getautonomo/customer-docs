# Intro to Templating

You have full control over how you communicate with your customers through emails and event descriptions. Our template editor allows you to finetune your copy to match your brand. And the powerful variables pull in all the data you need to tailor each email or event description to every order.

If you've never used a templating tool before, see the below example on how variables work to pull in data custom to each order. On the left is how you will program the template and on the right is what your customer will see for their order.

|             Variable            |       Output       |
| :-----------------------------: | :----------------: |
| Hello, \{{client\_full\_name\}} | Hello, Sarah Jones |

Double brackets "\{{" or "\}}" tell the system that we're looking for a variable, in this case, `"client_full_name"`. When this template email is fired off to the customer, the system will look for the client's name who submitted the order and replace `{{client_full_name}}` with "Sarah Jones," for example.

## Templating Overview

{% embed url="https://www.loom.com/share/4e49807446ba4f6c9ad4869e71a36d9d" %}

For a more thorough explanation, read on!

To see the tool in action, navigate to **Configure Booking** > **General** > and then you'll see two templates, **Send Confirmation Email** and **Calendar Events**. Let's start with **Send Confirmation Email,** so go ahead and click **Edit Template** to its right.

![](<../.gitbook/assets/1 - Overview.png>)

On the left is the email that your customers will see, and on the right is the editor. As you make changes on the right in the editor, you will see those changes as your customer will see them on the left. You don't need to click **Save template** every time you make a change to update the view on the left.

## Template Editor

Taking a closer look at the editor view on the right, you can see we can change the email subject. Below that, some formatting tools like you would find in Microsoft Word. Then in the body of the editor, we've highlighted one example of how you can use variables to communicate information about a specific order. In this example, the text "Project Square Footage" will display as "Project Square Footage," but the _variable_ `{{property_square_footage}}` will instead be automatically translated by the system to that order's square footage, for example, "1,333".\
\
When you're done editing, make sure to click the **Save template** purple button!

{% hint style="danger" %}
When using variables, you must be _exact._ `{{property_square_footage}}` and `{property_square footage}}` may look similar, but that second missing "\_" between "square" and "footage" will break the variable, and we won't replace the variable with any data.
{% endhint %}

## Template Data

That is one simple example, but as you can see in your pre-populated template, you can use as many variables in an email as you want! The complete list of available variables is here [here](variables.md), but you can also see more to the left of the editor under the tab Template Data.

![](<../.gitbook/assets/3 - Template Data.png>)

In the highlighted example, the text in purple `property_square_footage` is the variable, and "1333" in red is the data this example order would populate for that variable. The text in red serves as an example because the name of the variable may not be clear at first glance.

To get more information on each of the variables available to you, continue to the [next section](variables.md).

## Removing Spaces

If your template has too many empty lines, you can reduce these by condensing variable arguments onto the same line. For example, the below template has a lot of unecessary empty space after the final sentence.

![](<../.gitbook/assets/image (43).png>)

By condensing the arguments a bit, the space is reduced to a more natural length:

![](<../.gitbook/assets/Variables After.png>)



## Enhanced Client Confirmation Emails with Time Slot - Specific Details

How to Set Up Enhanced Client Confirmation Emails with Time Slot-Specific Details

We’ve upgraded the client confirmation email system to include time slot-specific service and provider details.  You can include what services will be completed on what date and by which provider, giving clients a clearer picture of their scheduled appointments.  You can set this up by editing your confirmation email template under Configure Booking > General, or by reaching out to our support team for assistance.

How to Edit Your Email Template:

1. Go to Configure Booking > General in your account settings.
2. Locate and select the Confirmation Email Template.
3. Customize the template to include the following dynamic fields (if not already present):
4.  {Service\_Date} – The date of the scheduled service

    {Service\_Name} – The name of the booked service

    {Provider\_Name} – The assigned provider for the service
5.  Save your changes.

    \


    \


    \


    \


\
