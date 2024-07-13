# Display Each Item

Some orders may have multiple if an order has multiple listing Agents, you will want to display each of the listing agents on that order. Below are examples of commands to accomplish this that you can copy/paste into your template.\
\
These commands may already be in your template, but please refer back here and copy/paste if you delete them.

## Listing Agent

| command                                                                                                                                                                                                | Output                                                                                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>{{#each listingAgents}}<br>Name: {{this.displayName}}<br>Phone: {{this.phone}}<br>Email: {{this.email}}<br>Brokerage: {{this.brokerage}}<br>License Number: {{this.licenseNumber}}<br>{{/each}}</p> | <p>Name: Sarah Jones</p><p>Phone: (111) 111-1111</p><p>Email: Sarah@company.com</p><p>Brokerage: Go for Broke</p><p>License Number: 123456</p><p></p><p>Name: Bobby Jones</p><p>Phone: (222) 222-2222</p><p>Email: Bobby@company.com</p><p>Brokerage: Go for Broke</p><p>License Number: 234567</p> |

This command lists all listing Agents on an order, whether it's 1, 2, or even more. If you want to remove some of the information, like the brokerage, for example, delete the whole line "Brokerage: \{{this.brokerage\}}".

{% hint style="info" %}
If you alter this command, do not change `{{#each listingAgents}}` or `{{/each}}` as that will break the command.
{% endhint %}

## Services

| command                                                                                                                                                                                                       | Output                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p> <strong>Booked packages and services</strong>{{#if package}}<br>{{package}}<br>{{#each services}}<br>- {{this}} {{/each}} {{/if}} {{#each services_a_la_cart}}<br>- (a la cart) {{this}}<br>{{/each}}</p> | <p></p><p><strong>Booked packages and services</strong></p><p>Luxury Package</p><ul><li>Home Photos</li><li>Drone Photo</li><li>Drone Video</li><li>(a la cart) 3D Matterport</li><li>(a la cart) Dedicated Listing Website</li></ul> |

This command lists the name of the package (if any), then all of the services within that package, then any services selected that are not part of that package. It also formats it into a bulleted list nested under the package name. We do not recommend making changes to this command as almost all components are necessary to function

## Package OR Services

|                                                                                                                                                  |                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| command                                                                                                                                          | Output                                                       |
| \{{#if package\}} \{{package.name\}} \{{else\}}\{{#each services\_a\_la\_cart\}}\{{this\}}\{{#unless @last\}}, \{{/unless\}}\{{/each\}}\{{/if\}} | <p>Luxury Package</p><p>OR</p><p>Photo, Video, 2D Layout</p> |

This command will display the Packages the customer ordered IF there is one. If the customer ordered only Services and no Packages, it will display a list of all\* Services ordered.

\*Be careful, it lists **all** Services, whether that is 1 or 10. So if you use this in Subject lines for emails or calendar events, they may get quite long.
