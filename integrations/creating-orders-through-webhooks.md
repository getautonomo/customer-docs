# Creating Orders Through Webhooks

{% hint style="warning" %}
This method of creating orders through webhooks is currently intended to be used for CBLC Listing Concierge. If you have questions about how you might be able to use webhooks to create orders from other sources, reach out to our support team.
{% endhint %}

## Limitations

* Each order can only include one Service OR one Package
* We do not enforce booking flow settings like pay-before-delivery for these orders
* You can only have two listing agents per order
* We do not include Agent Photo or Brokerage Logo, you must manually collect it and add it to the order
* We do not include Custom Tiers, you must add those after the order comes through
* The date must be in the MM/DD/YYYY format
* You will need to manually add the address to the order
* You will need to have a [Zapier ](https://zapier.com/)account

## Setup Steps

### Receive orders through Email

For this feature to work, you must receive emails in a standard format. The information for every order must be in the same format and location in that email every time.

You can set up this feature for multiple types of forms. So for example, the email from CBLC may look different than another brokerage, but as long as all of the CBLC emails look the same and all the other brokerage's emails look the same, this will work.

This is an example of a form email that is compliant with our system:

![](<../.gitbook/assets/image (80).png>)

However, it doesn't have to be as formatted as that, for example, this one also works:

![](<../.gitbook/assets/image (87).png>)

The important thing is that the format is the same _every time_. That is why we call them "form emails". The only thing different between one email and the other is the order details.

### Parse the Email

"Parse" in this context means for a computer to read an email and put the right fields into an order. For example, we'll automatically read the email and understand that "Premier Package" is the Package of Services that the customer wants to order. We'll then set the Services on the order to be those within the Premier Package.\
\
However, first, you need to teach our system the format of your email that contains the order.

Zapier has a help article on setting up their email parser [here](https://parser.zapier.com/).

See our Variables section below for what information you can parse in Zapier.

We highly, highly recommend you put the entire email in `additional_notes`

### Variables

There are a number of pieces of information we can use in creating an order. These pieces of information are all _optional_. You should parse as much information as you can into the order so that it's automated, but you don't _have_ to.

<table data-header-hidden><thead><tr><th width="267.61458846722525">Variable</th><th>Example</th><th>Explanation</th></tr></thead><tbody><tr><td>Variable</td><td>Example</td><td>Explanation</td></tr><tr><td><code>booking_flow_address</code></td><td>CBLC</td><td>Each booking flow has a unique url that you can set with <a href="../services-and-packages/booking-flows.md">these instructions</a>. If left empty, we default to your primary booking flow.</td></tr><tr><td><code>service_or_package</code></td><td>Premier Package</td><td>Must be the exact name of one of your Services or Packages found in the Booking Flow.</td></tr><tr><td>{{#each service_custom_tiers}}{{serviceName}} - {{<a href="http://selected.name">selected.name</a>}}{{/each}}{{/if}}</td><td></td><td>Lists each of the custom tiers selected per service</td></tr><tr><td><code>order_name</code></td><td>Permier Package - 12345 Main Street, Springfield, OR, 12345 - Bob Jones</td><td>You can set the Order Name to be what you want, or leave it blank and we'll default to the Services or Package + address + client name</td></tr><tr><td><code>client_full_name</code></td><td>Bob Jones</td><td>The name of the person making the order (not necessarily the Agent for the order)</td></tr><tr><td><code>contact_notes</code></td><td>sarahjones@brokerage.com</td><td>The email addresses for other people that should be included on an order</td></tr><tr><td><code>email</code></td><td>bobjones@brokerage.com</td><td>The contact email address for the person making the order (not necessarily the Agent for the order)</td></tr><tr><td><code>phone_number</code></td><td>1235467890</td><td>The contact phone number for the person making the order (not necessarily the Agent for the order). We will remove spaces, dashes, and parenthesis.</td></tr><tr><td><code>property_address_formatted_address</code></td><td>12345 Main Street, Springfield, OR, 12345</td><td>The formatted address of the property for the shoot.</td></tr><tr><td><code>property_address_line2</code></td><td>Apt 2</td><td>Apt or Suite number</td></tr><tr><td><code>rooms_bedrooms</code></td><td>1</td><td>Number of Bedrooms</td></tr><tr><td><code>rooms_bathrooms</code></td><td>2</td><td>Number of Bathrooms</td></tr><tr><td><code>rooms_half_baths</code></td><td>3</td><td>Number of Half-Baths</td></tr><tr><td><code>property_square_footage</code></td><td>1500</td><td>The square footage for the property. We will remove any commas.</td></tr><tr><td><code>property_feature_notes</code></td><td>The views.</td><td>The answer to the question "What amenities or unique features would you like us to feature?"</td></tr><tr><td><code>entry_notes</code></td><td>I will meet you there.</td><td>The answer to the Entry Notes question</td></tr><tr><td><code>date</code></td><td>06/30/2022</td><td>The <strong>requested</strong> date of the shoot in MM/DD/YYYY format</td></tr><tr><td><code>scheduled_time</code></td><td>12:00 PM</td><td>The <strong>requested</strong> time of the shoot</td></tr><tr><td><code>brokerage_code</code></td><td>CBLC</td><td>If the agent has a brokerage code</td></tr><tr><td><code>custom_domain</code></td><td>1234mainstreet.com</td><td>If the agent wants a custom domain for their Website</td></tr><tr><td><code>music_option</code></td><td>dropbox.com/musicoptions/1</td><td>The URL to the music they want</td></tr><tr><td><code>floor_plans_notes</code></td><td>Detached garage</td><td>The answer to the question: "If you have chosen to book a 3D Virtual Tour and/or 2D Floor Plan; is there an ADU; garage; or additional space you would like to include?"</td></tr><tr><td><code>order_notes</code></td><td>Please arrive 15 minutes early.</td><td>The answer to the question: "Is there anything else we can help you with or that we should know?"</td></tr><tr><td><code>existing_contact</code></td><td>Salesperson Sally</td><td>The answer to the question: "Are you working or speaking with anyone on our team already on this project?"</td></tr><tr><td><code>additional_notes</code></td><td></td><td>The "additional notes" section of orders in Order Management. We highly recommend putting the original email in this field for reference.</td></tr><tr><td><code>listing_agent_name</code></td><td>Bob Jones</td><td>The first and last name for the first agent on the listing.</td></tr><tr><td><code>listing_agent_brokerage</code></td><td>CBLC</td><td>The brokerage for the first agent on the listing.</td></tr><tr><td><code>listing_agent_phone</code></td><td>1234567890</td><td>The phone number for the first agent on the listing.</td></tr><tr><td><code>listing_agent_email</code></td><td>bobjones@cblc.com</td><td>The email address for the first agent on the listing.</td></tr><tr><td><code>listing_agent_license_number</code></td><td>12345</td><td>The license number for the first agent on the listing.</td></tr><tr><td><code>listing_agent_name2</code></td><td>Sally Jones</td><td>The first and last name for the second agent on the listing.</td></tr><tr><td><code>listing_agent_brokerage2</code></td><td>CBLC</td><td>The brokerage for the second agent on the listing.</td></tr><tr><td><code>listing_agent_phone2</code></td><td>0987654321</td><td>The phone number for the second agent on the listing.</td></tr><tr><td><code>listing_agent_email2</code></td><td>sallyjones@cblc.com</td><td>The email address for the second agent on the listing.</td></tr><tr><td><code>listing_agent_license_number2</code></td><td>54321</td><td>The license number for the second agent on the listing.</td></tr></tbody></table>

### Webhook Endpoint

During the parse set up, Zapier will ask you for your webhook URL. Your URL follows this format:

`portal.yourdomain.com/webhooks/create-order`

So for a photo company called **Real Estate Media**, there's would be `portal.realestatemedia.com/webhooks/create-order`

### Tonomo Creates an Order

Within a couple of minutes of receiving an email with an order, Zapier will parse the email, send it to Tonomo and we will create an order in the Pending Status.

We highly recommend you review the order for any missing components that the parser couldn't understand and add them. This is why we recommend putting the original email in the Additional Notes.
