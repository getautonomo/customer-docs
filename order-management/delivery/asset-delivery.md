# Asset Delivery

{% embed url="https://www.loom.com/share/edeebaff2eb9415d85a3bff9abf46182?sid=439840a4-c67c-45c8-bd1a-0b836bb548c6" %}

### Overview

Tonomo can help you save time and deliver your project files to your customers in a beautiful and professional manner.

* Integrates with dropbox and automatically creates the folder structure based on the services that are booked
* Automatically process your full size images and deliver different resolutions to your customers
* Creates a beautiful photo and video gallery that agents can access through their customer portal.

![](<../../.gitbook/assets/image (1) (1) (1) (1).png>)

### Configure

To get started you need to connect your Dropbox account which you can do under **Configure Booking** and **General.**

![](<../../.gitbook/assets/Dropbox Config.png>)

Next, enter a root folder. What we mean by "root folder" is a folder where all of your Tonomo orders and files are going to live. This might be called "Projects", "Orders", or "Deliverables." Tap **Save**.

{% hint style="info" %}
Your root folder must be the **Share** link. Don't just copy/paste the URL from your browser address bar.
{% endhint %}

![](<../../.gitbook/assets/image (51).png>)

### Prerequisites

Before we will create Dropbox folders for you, an order must meet a few requirements. The order must have:

* [ ] A customer email and agent
* [ ] An address
* [ ] At least one service

If your order comes through the normal booking flow, you will have all of this information and you can proceed with delivering the order. We point this out, however, because it's possible to create an order through a [manual method](../creating-orders-for-your-customers.md#manual-method) as an admin that doesn't _force_ you to enter this information. So it's possible to have an order missing these prerequisites.

### Using the Dropbox Link

Once an order meets the above prerequisites, we will create dropbox folders for your order once it enters In Progress or Completed.

You can find your dropbox link for your order on the Order Details panel on the right of Order Management after you've clicked on the order in question.

![](<../../.gitbook/assets/Deliverables Link.png>)

This is not the link you will send to customers, this is the link your staff will use to upload the assets for the order. If you click that arrow-in-a-box icon it will take you to your folder in Dropbox.&#x20;

Within that folder you will see one folder for each of your Services, for example; "Home Photos," "2D Layout," and "Drone Video." Your staff will upload the assets that go into each folder directly.

If you do not want us to create a folder for a Service, say, Twilight Photos, where you prefer to just include the Twilight Photos in the same folder as the Listing Photos, you can control this under **Configure Booking** > **Services**. Once there, in the column **Service Type** you can set it to **None**. This means we will not create a unique folder for that Service.

![](<../../.gitbook/assets/Service Type (1).png>)

Your staff only need to upload full sized assets. We will momentarily create MLS resized assets for you. Once we do, we move the full-size assets into one folder and the MLS resized assets into another nested within the parent folder for that Service.

### Video

There are two ways you can deliver video assets. You can just upload the file in full and the agent can download it. But you can also give them a Vimeo or Youtube link (and you can of course do both!)

Whether you deliver with a Vimeo/Youtube link or a file, we'll display that video on the asset delivery page so that everything is presented in one, sleek location.

![](<../../.gitbook/assets/image (162).png>)

{% hint style="info" %}
For us to preview your video on the delivery page, it must be in the .mp4, .mov, .webm, or .3gp filetype
{% endhint %}

To add a Vimeo or Youtube link, just copy the URL and click Create > More > Shortcut and add it to the same dropbox folder as where you uploaded the whole file.

![](<../../.gitbook/assets/image (50).png>)

If you want to offer a Youtube/Vimeo link **and** full files for download, we will default to preview the Youtube/Vimeo link. To preview the full files, click Edit Links and delete the Youtube/Vimeo link.

![](<../../.gitbook/assets/image (14) (1).png>)

### Creating Delivery Links

Once your assets have been uploaded and you're ready to deliver to your client, navigate back to the Deliverables section of Order Details and click **Sync Delivery Files**.

![](<../../.gitbook/assets/image (174).png>)

When you click this button, we do a few things:\
\
First, we convert your full-sized assets into MLS assets and get everything organized. Give this between a few seconds and a minute or so depending on the number of images.

Second, we will be creating for you a formatted delivery page so that your customers can get a beautiful preview of your work before they download.

If you're ready to deliver the order, scroll up on the right-hand bar and move the **Order Status** to **Completed**. Click the icon in the top right to grab your project delivery link for the customer. You can send this link as the final deliverable link to the customer, but we will have emailed them the link as well when you moved them to Completed.

![](<../../.gitbook/assets/Deliverables Link (1).png>)

## How to sync multiple delivery files in bulk

Sync multiple ready-to-deliver orders at once instead of processing them individually.

Steps to Bulk Sync Delivery Files

1. Navigate to the Orders section in your dashboard.
2. Check the box next to each order you want to sync.
3. As you select orders, a "Sync Delivery Files" button will appear at the bottom of the screen.
4. Click "Sync Delivery Files" to process all selected orders at once
5. Wait for confirmation that the sync is complete.

<figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure>

## Preview Assets

If you are using our Integrated Payments feature, and your customers must pay before downloading their assets, then Tonomo allows them to **preview** their assets before paying. We block the ability for them to download the assets until the order is flagged as **Paid**.

{% embed url="https://www.loom.com/share/c44eb2fa31ce4e39a850cb902c8b744d" %}
