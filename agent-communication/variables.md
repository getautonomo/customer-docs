# Variables

## Available Variables

What follows are tables of all the variables we support. In the left column is the variable itself. In the center is an example of what it would look like in an email. On the right is more information about that variable. You are welcome to use this as a guide to copy/paste the variables to your template. Ensure you get both of the opening \{{ and closing \}} brackets!

More information on how to use:

{% embed url="https://www.loom.com/share/4e49807446ba4f6c9ad4869e71a36d9d" %}

### Order Details

<table data-header-hidden><thead><tr><th width="276.3333333333333">Variable</th><th>Example</th><th>Explanation</th></tr></thead><tbody><tr><td>Variable</td><td>Example</td><td>Explanation</td></tr><tr><td><code>{{order_name}}</code></td><td>12345 Main Street, Springfield, OR, 12345 - Sarah Jones</td><td>The name of the order as it is displayed in Order Management under the column "Services"</td></tr><tr><td><code>{{dateCreated}}</code></td><td>May 4, 2021</td><td>The date the order was created</td></tr><tr><td><code>{{date}}</code></td><td>May 10, 2021</td><td>The scheduled date of the shoot.</td></tr><tr><td><code>{{scheduled_time}}</code></td><td>11:00 am - 2:00 pm</td><td>The scheduled time of the shoot</td></tr><tr><td><code>{{orderId}}</code></td><td>PXhSdRzsfiUYVfSg4ewY</td><td>The order's unique identifier in the system. You can search with this or tack it onto a URL to create a link directly to the order (see <a href="variables.md#hyperlinks">here</a>)</td></tr><tr><td><code>{{orderStatus}}</code></td><td>pending</td><td>The order's status in fulfillment, from pending, to in progress, to completed</td></tr><tr><td><code>{{invoice_amount}}</code></td><td>650</td><td>The amount of the invoice. Note: this does not include the dollar sign, so write the variable as "${{invoice_amount}}" and that will display as "$650"</td></tr><tr><td><code>{{invoice_link}}</code></td><td>quickbooks.com/invoice/123456</td><td>If you have already entered the invoice for this order, it will display here</td></tr><tr><td>https://portal.[domain].com/order-status/{{orderId}}/invoice</td><td>https://portal.tonomo.io/order-status/{{orderId}}/invoice</td><td>This links to a publicly viewable invoice for the order where they can review, download, and pay the invoice</td></tr><tr><td><code>{{deliverable_link}}</code></td><td>dropbox.com/folder/123456</td><td>If you have already entered the dropbox link for this order, it will display here</td></tr><tr><td>https://portal.[domain].com/order-status/{{orderId}}/reschedule</td><td>https://portal.tonomo.io/order-status/{{orderId}}/reschedule</td><td>Direct link to where the customer can reschedule the order themselves (if you have Self-Reschedule <a href="https://docs.getautonomo.com/scheduling/scheduling-configuration/allow-customers-to-reschedule-and-cancel-on-their-own">turned on</a>)</td></tr><tr><td>https://portal.[domain].com/order-status/{{orderId}}/cancel</td><td>https://portal.tonomo.io/order-status/{{orderId}}/cancel</td><td>Direct link to where the customer can cancel the order themselves (if you have Self-Reschedule <a href="https://docs.getautonomo.com/scheduling/scheduling-configuration/allow-customers-to-reschedule-and-cancel-on-their-own">turned on</a>)</td></tr></tbody></table>

### Project Details

| Variable                                                                                                                                                  | Example                                                   | Explanation                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `{{property_address.lng}}`                                                                                                                                | 11.6984987                                                | The longitude of the project address                                                                                                                      |
| `{{property_address.lat}}`                                                                                                                                | 48.1394899                                                | The latitude of the project address                                                                                                                       |
| `{{property_address.placeId}}`                                                                                                                            |                                                           | A unique identifier for Google Maps. No practical purpose                                                                                                 |
| `{{property_address.line2}}`                                                                                                                              | Apt. #1234                                                | The second line of an address, like apartment number                                                                                                      |
| `{{property_address.formatted_address}}`                                                                                                                  | 12345 Main Street, Springfield, OR, 12345                 | The formatted version of the address                                                                                                                      |
| `{{property_square_footage}}`                                                                                                                             | 1000                                                      | The square footage of the property                                                                                                                        |
| `{{package.name}}`                                                                                                                                        | Luxury package                                            | The package, if any, the customer selected when booking                                                                                                   |
| `{{package.agentCode}}`                                                                                                                                   | COMPASS                                                   | The package's Custom Package code, if any                                                                                                                 |
| `{{package.PackageID}}`                                                                                                                                   | voZqb9FhgE7SnfrvrZWK                                      | The package's ID code that Tonono assigns                                                                                                                 |
| `{{services}}`                                                                                                                                            |                                                           | A list of all services that are part of a package. See [this article](display-each-item.md#services) for more information to display your services        |
| `{{services_a_la_cart}}`                                                                                                                                  |                                                           | All services selected that are **not** part of a package. See [this article](display-each-item.md#services) for more information to display your services |
| \{{#if service\_custom\_tiers\}} Custom service options: \{{#each service\_custom\_tiers\}} \{{serviceName\}} - \{{selected.name\}} \{{/each\}} \{{/if\}} | <p>Custom service options:<br>Photography - 10 Photos</p> | IF there are any Services with a Custom Tier option, list those Services and their Custom Tier                                                            |

### Agents

| Variable               | Example           | Explanation                                                                                                                                                                                                                                              |
| ---------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `{{client_full_name}}` | Sarah Jones       | The first and last name of the person who booked the order                                                                                                                                                                                               |
| `{{email}}`            | sarah@company.com | The email address of the person who booked the order                                                                                                                                                                                                     |
| `{{phone_number}}`     | (555) 555-5555    | The phone number of the person who booked the order                                                                                                                                                                                                      |
| `{{brokerage_code}}`   | CWB               | If the agent book using one of your agent codes for a custom package, we will display that code here                                                                                                                                                     |
| `{{listingAgents}}`    |                   | The contact information and branding for the listing agents on the order. As there can be multiple, we recommend an `each` argument so that you display all listing Agents involved. [See here for more information](display-each-item.md#listing-agent) |

| Variable                  | Example                    | Explanation                                               |
| ------------------------- | -------------------------- | --------------------------------------------------------- |
| \{{photographers.name\}}  | John Smith                 | The first and last name of the photographer on the order. |
| \{{photographers.phone\}} | +11005551234               | The phone number and area code of the photographer        |
| \{{photographers.email\}} | johnsmith@photographer.com | The email of the photographer                             |

### Additional Notes

| Variable                     | Example                   | Explanation                                                                                                                                                 |
| ---------------------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `{{floor_plan_notes}}`       | Include garage            | Displays notes, if any, the agent entered for floor plans when booking                                                                                      |
| `{{contact_notes}}`          | assistant@company.com     | Displays email(s), if any, the agent wanted included on any communication                                                                                   |
| `{{property_feature_notes}}` | Feature the views         | Displays notes, if any, the agent entered for unique amenities or features when booking                                                                     |
| `{{existing_contact}}`       | John Smith                | Displays the name of the employee the Agent indicated they were working with, if any                                                                        |
| `{{calendarEvent}}`          | 9o18z099vs21om3om1sk5hsxo | The unique calendar ID for the booking. No practical use at the moment                                                                                      |
| `{{entry_notes}}`            | The code is 1234          | Displays notes, if any, the agent entered for entry notes when booking                                                                                      |
| `{{preferred_contact}}`      | call                      | Displays the method of communication the Agent indicated in their profile                                                                                   |
| `{{custom_domain}}`          | 123mainstreet.com         | Displays the custom domain, if any, they entered for their order                                                                                            |
| `{{order_notes}}`            | Must not shoot in rain    | Displays notes, if any, the Agent entered when we asked them if there was anything else we can help them with or that we should know                        |
| `{{music_option}}`           | soundstripe.com/12345     | The URL to the music the client selected, if any                                                                                                            |
| `{{members}}`                |                           | Legacy code. Generally unused                                                                                                                               |
| `{{customQuestions}}`        |                           | These are custom questions you entered for your orders. Notice they are nested, so to use them type \{{customQuestions.\[nested variable in purple here]\}} |

### Single Property Websites

|                        |                                       |                                                                                                                  |
| ---------------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Variable               | Example                               | Description                                                                                                      |
| \{{spw.urlBranded\}}   | listings.company.com/1234-main-street | Every Single Property Website can have it's own Branded URL you or the Agent sets.                               |
| \{{spw.urlUnbranded\}} | listings.company.com/best-home-ever   | Because you can set different URLs for Branding/Unbranded versions, you can specify to add the Unbranded as well |

## Nested Variables

You may notice some variables are nested within other variables in the [Template Data](intro-to-templating.md#template-data) section. You can see these by clicking the little arrow to the left of variables like `{{property_address}}`

![](<../.gitbook/assets/4 - Nested Variables.png>)

So `{{property_address}}` is the parent variable and `{{lng}}`, `{{placeId}}`, `{{formatted_address}}` are all variables nested underneath it. To communicate the formatted address for this order, you need to include the parent and nested variable, shown like this; `{{property_address.formatted_address}}`. That "." is what instructs the system to look under `{{property_address}}` to find `{{formatted_address}}`and in this example, it would just be displayed as "Paul-Henri-Spaak-Straße 12, 81829 München, Germany".

## Hyperlinks

You may also use variables in hyperlinks. For example, if you want to link to the Order Status page for the order they just submitted, create a hyperlink for a piece of text and in the URL, enter\
`portal.yourdomain.com/order-status/{{orderId}}`

Then, when your agent clicks that link, they will be routed to the Order Status page for their order!

{% hint style="info" %}
Note, you need to replace "yourcompany" with your domain.
{% endhint %}
