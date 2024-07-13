# Configuring Email DNS Records

Tonomo handles a lot of the email communication you'll be making with your customers automatically. But we do require one step on your end and that is updating your website's DNS records so that our emails come from your domain instead of a generic one. With these steps done, we'll send out emails for you from @companyname.com so that everything stays on-brand.

## What you'll need

* [ ] Admin credentials to your DNS provider (see below if you do not know who this is)
* [ ] DNS records from your Tonomo onboarder or support agent

## DNS Provider

DNS provider is the company or service that lets you manage and change your DNS records. If you do not know who this is, go to [who.is](https://who.is/) and search for your website. In the results will be a section called Nameservers. The domain for these name servers will be your DNS provider.

![](<../.gitbook/assets/Name Servers.png>)

In this example, we know that we'd need admin credentials to googledomains.com to change our DNS records. Every DNS provider has their DNS records in a different section of their website. If you Google "\[DNS provider] change DNS Records" (where "\[DNS provider]" is the name of the DNS provider) you will usually find an article on how to navigate to your DNS records settings.

If you have trouble finding your settings, reach out to your Tonomo onboarder or support agent.

## DNS Records

Now that we're in your DNS provider's settings page with your admin credentials, we need to make a few changes. We need to create 3-5 DNS records. Each record is going to have a **Type** like "MX", "TXT", or "CNAME". They will also have a **Host** that will look like a normal website like 12345.companyname.com. Finally, they'll have a **Value** which could be anything from a website like mx.sendgrid.net or long strings of random numbers and letters. The good news is we can copy/paste these!

{% hint style="info" %}
If your Tonomo onboarder or support agent hasn't already sent you your DNS records, reach out to them to get that information. You will not be able to continue without this information.
{% endhint %}

Add each of the DNS records that you receive from Tonomo support. If you receive an error that your DNS provider does not let you enter underscore (\_) characters in your CNAME records, reach out to your Tonomo support agent. They will have make a change to your settings and get you new DNS records. Once done, let your Tonomo support agent know and they will verify your DNS records. Frequently these are verified by the system quickly, but can take up to 24 hours, or in extreme cases, 48 hours. Your Tonomo support agent will let you know when you're all verified or if additional steps are needed.\
\
You're all set! If your DNS provider does not accept underscore (\_) characters, you may have to update these records in the future, but your Tonomo support agent will let you know if/when that needs to be done!

## Common DNS Providers

Wix

[https://support.wix.com/en/article/managing-dns-records-in-your-wix-account](https://support.wix.com/en/article/managing-dns-records-in-your-wix-account)

Google Domains

[https://support.google.com/domains/answer/3290350?hl=en](https://support.google.com/domains/answer/3290350?hl=en)

Squarespace

[https://support.squarespace.com/hc/en-us/articles/360002101888-Adding-custom-DNS-records-to-your-Squarespace-domain](https://support.squarespace.com/hc/en-us/articles/360002101888-Adding-custom-DNS-records-to-your-Squarespace-domain)

GoDaddy

[https://www.godaddy.com/help/manage-dns-records-680](https://www.godaddy.com/help/manage-dns-records-680)

