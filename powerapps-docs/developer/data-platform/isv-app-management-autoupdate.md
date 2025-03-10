---
title: Auto app updates (preview) | Microsoft Docs
description: Learn about the latest auto update feature for apps.
ms.date: 03/22/2023
author: angela21k
ms.author: angelakim
ms.reviewer: jdaly
suite: powerapps
ms.topic: article
ms.subservice: dataverse-developer
search.audienceType: 
  - developer
search.app: 
  - PowerApps
contributors: 
  - JimDaly
---

# Auto app updates (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](../../includes/cc-beta-prerelease-disclaimer.md)]

Auto app update feature allows automatic updates of third-party applications installed through AppSource. This feature helps both third-party  publishers and customers keep software up to date in a simple and controlled way with minimal administrative overhead.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren't meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.

Automatic updates in the preview will be limited to:  

- **Explicit tenant admin opt-in**: Tenant administrator user must opt-in from the Power Platform admin center to enable the feature.

- **Pre-approved publishers**: Tenant administrator user must indicate which third-party publishers are permitted to automatically update apps in their environment once opted-in from the Power Platform admin center.

- **Dark hours only**: To further minimize impact, automatic updates will only happen during dark hours defined by either the customer or at geo level.  

## Enabling auto app update  

> [!NOTE]
> Publishers do not require additional action to enable automatic updates for their apps. Only tenant admin users are required to act if they want to opt-in to this feature for select third-party publishers.

1. Log into the [Power Platform admin center](https://admin.powerplatform.microsoft.com) as an administrator user. From the Environments page, select an environment and click on **Settings**.

   :::image type="content" source="media/auto-app-update-0.jpg" alt-text="Power Platform admin center environment":::

1. From the environment settings page, under the **Updates** section, click to open the **App update settings** page.  

   :::image type="content" source="media/auto-app-update-1.jpg" alt-text="Power Platform admin center environment settings":::

1. Toggle the configurator to **'On'** to opt-in to the feature.  From the drop-down list of publishers, select for which third-party publishers you want to automatically update apps.

   > [!NOTE]
   > The drop-down list will only display publishers if you have a third-party application installed.

   :::image type="content" source="media/auto-app-update-2.jpg" alt-text="Configure app update settings":::

1. Click **Save** to keep your changes.


## Monitoring opt-in environments in ISV Studio

As a publisher with access to ISV Studio, you can view details about your automatic updates and opt-in rates.
 
1. Login to [ISV Studio](https://isvstudio.powerapps.com/). From the navigation menu, click on **Analytics** and **Published apps**, **Graphical user interface**, and then application.

   :::image type="content" source="media/auto-app-update-3.jpg" alt-text="ISV Studio published apps":::
 
1. Select a specific app and click the **Auto Updates** tab to view opt-in rates for publishers and environments, which organizations have opted out, as well as a detailed list of version history.

   :::image type="content" source="media/auto-app-update-4.png" alt-text="ISV Studio Auto Updates tab":::

1. From the **Version Update History** table, click **View Details** to view details about the deployment status by region.

   :::image type="content" source="media/auto-app-update-5.jpg" alt-text="ISV Studio version update details":::

> [!NOTE]
> The **Cancel Deployment** button will cancel automatic updates for any regions with release status in progress or to be scheduled.

### See also

[Introduction to ISV Studio for the Power Platform](isv-app-management.md)  
[Home page](isv-app-management-homepage.md)<br/> 
[App page](isv-app-management-apppage.md)<br/> 
[AppSource checker](isv-app-management-appsource-checker.md)<br/> 
[Connector Certification](isv-app-management-certification.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
