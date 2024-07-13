# Allow Customers to Reschedule and Cancel on their Own

If your customers want to reschedule or cancel their order, they can do that without contacting you. We'll update the Tonomo portal with their requested changes and the calendar app will send updates to all emails on the order.

## Setup

You have control over some settings on if and when customers can reschedule under each Booking Flow's settings:

![](<../../.gitbook/assets/image (143).png>)

## Get your Links

You can include these links in your calendar description and automated emails. Just copy and paste the below URLs into your calendar description or email template, with your domain instead of \[domain]. We'll fill in the Order ID for every order

<table><thead><tr><th width="200.8770408562416">Use</th><th>URL</th></tr></thead><tbody><tr><td>Cancel</td><td>https://portal.[domain].com/order-status/{{orderId}}/cancel</td></tr><tr><td>Reschedule</td><td>https://portal.[domain].com/order-status/{{orderId}}/reschedule</td></tr></tbody></table>

If you need to send a link to a specific customer in a text or something out of Tonomo, you need to replace \{{orderId\}} with the order's ID. To find that, just open the order in Tonomo and the Order ID will be in the URL. The Order ID is everything between "orderId=" and "\&filter"

![](<../../.gitbook/assets/image (133).png>)

Once they click those links, they'll be taken to a page where they can cancel or reschedule the order:\


![](<../../.gitbook/assets/image (71).png>)
