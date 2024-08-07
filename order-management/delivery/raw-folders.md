# Raw Folders

## Raw Folders

Tonomo can create your folders for raw assets that your editors can then access. To enable this feature, navigate to your **General** settings under **Configure Booking.** Toggle on the Create RAW Folders button.

By default, we will create a folder within your Root Dropbox Folder called "Raw Files." However, you may manually create a folder and input that link and click **Save**.

{% hint style="warning" %}
If you enter an alternative Dropbox link for raw files, it **must** be on the same Dropbox account that is connected above.
{% endhint %}

![](<../../.gitbook/assets/image (7).png>)

Once enabled, all future orders that have their folders created will generated raw folders according to this structure

* Root Folder
  * Raw Folder
    * Photographer Name (Name of photographer assigned to the order when the folder structure was created. If there are two, we pick the first alphabetically)
      * Scheduled Date of the Shoot
        * 1 Folder for each service that has a [Service Type](https://docs.getautonomo.com/services-and-packages/services#service-type)

{% hint style="warning" %}
Note: If you are **not** using the "Use integrated booking" feature for your booking flow the events are coming as time requests and not finalized dates, therefore, the raw folder will not be created it will require you to manually create an event in the scheduler to create the folder.&#x20;
{% endhint %}
