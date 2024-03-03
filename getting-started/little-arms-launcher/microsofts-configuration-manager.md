# ⭐ Microsoft's Configuration Manager

1. Create a content object in the Microsoft Configuration Manager

{% hint style="info" %}
The content object could contain the Little Arms Launcher & the Zephyr application, but we advise that they use separate content objects for each since Zephyr updates differently than the Little Arms Launcher
{% endhint %}

1. Once the content objects are created, you can use the Software Library in the Configuration manager to make those content objects available to the clients.
   1. You would use the client manager to tell the clients to download the content objects if they are out of date.
2. Where there is an update to the Zephyr or the Little Arms Launcher applications, you can update the files in those content objects and trigger an update cycle on the clients.
   1. That will update the sim silently to whatever they have placed in the content object.

Reference Guide: [Deploy Content - Configuration Manager](https://learn.microsoft.com/en-us/mem/configmgr/core/servers/deploy/configure/deploy-and-manage-content)
