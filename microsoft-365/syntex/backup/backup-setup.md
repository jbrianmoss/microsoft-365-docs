---
title: Set up Microsoft 365 Backup (Preview)
ms.author: chucked
author: chuckedmonson
manager: jtremper
audience: admin
ms.reviewer: sreelakshmi
ms.date: 01/17/2024
ms.topic: conceptual
ms.service: microsoft-syntex
ms.custom: backup
search.appverid:
ms.collection:
    - enabler-strategic
    - m365initiative-syntex
ms.localizationpriority:  medium
description: Learn how to set up and configure Microsoft 365 Backup and backup policies.
---

# Set up Microsoft 365 Backup (Preview)

> [!NOTE]
> Microsoft 365 Backup (Preview) is rolling out. When it is available worldwide, this message will be updated and you will be able to see and enable the feature in the Syntex billing setup flow in the Microsoft 365 admin center.

Get started with Microsoft 365 Backup by following the simple three steps in the Microsoft 365 admin center.

![Diagram showing the three-step setup process for Microsoft 365 Backup.](../../media/content-understanding/backup-setup-diagram.png)

<!---<insert how-to Affirma video   – https://aka.ms/M365Backup-how-to-video> --->

## Prerequisites

### Set up pay-as-you-go billing

As a first step to sign up for Microsoft 365 Backup, you should first link an Azure subscription in [Syntex pay-as-you-go](https://admin.microsoft.com/Adminportal/Home#/featureexplorer/csi/ContentUnderstanding), if you haven't already done so. Although Microsoft 365 Backup isn't part of the Syntex product suite, this offering is still using the Syntex billing setup for consistency with other Microsoft 365 pay-as-you-go offerings.

<!---
1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home).

2. Select **Setup**.

3. On the **Setup** page, in the **Files and content** section, select **Use content AI with Microsoft Syntex**.

4. On the **Use content AI with Microsoft Syntex** page, select **Set up billing**.

    ![Screenshot of the Use content AI with Microsoft Syntex page showing the Set up billing option.](../../media/content-understanding/backup-setup-set-up-billing.png)

    > [!NOTE]
    > To set up pay-as-you-go billing for Microsoft 365 Backup, the admin must have an owner or contribution role on the Azure subscription to be used.

5. If you don't have an Azure subscription or resource group, follow these steps. If you have an Azure subscription and resource group, skip this step and go to step 6.

    ![Screenshot of the Set up pay-as-you-go billing panel with the Prerequisites section lighlighted.](../../media/content-understanding/backup-setup-prerequisites.png)

    a. To create a new Azure subscription, on the **Set up pay-as-you-go billing** panel, select **Learn more about Azure subscriptions**. Alternatively, you can follow the steps in [Create your initial Azure subscriptions](https://learn.microsoft.com/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions).

    b. To create a new Azure resource group, on the **Set up pay-as-you-go billing** panel,select **Learn more about Azure resource groups**. Alternatively, you can follow the steps in [Manage Azure resource groups by using the Azure portal](https://learn.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal) to create a resource group. The resource group should be within the Azure subscription.

    c. After you create an Azure subscription with owner or contributor role, you'll need to have a resource group created.

6. If you have an Azure subscription, select the subscription from the drop-down menu.

    ![Screenshot of the Set up pay-as-you-go billing panel with the Azure subscription section lighlighted.](../../media/content-understanding/backup-setup-azure-subscription.png)
--->
To set up pay-as-you-go billing, follow the steps in [Configure Microsoft Syntex for pay-as-you-go billing](../syntex-azure-billing.md).

### Permissions

You must have Global admin or SharePoint admin permissions to access the Microsoft 365 admin center and set up Microsoft 365 Backup.

### Enable Microsoft 365 Backup

To enable Microsoft 365 Backup, you'll need to go to the Microsoft 365 admin center.

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home).

2. Select **Setup**.

3. On the **Setup** page, in the **Files and content** section, select **Use content AI with Microsoft Syntex**.

4. On the **Use content AI with Microsoft Syntex** page, select **Manage Microsoft Syntex**.

5. From the list of products, select **Backup Preview**.

6. By default, the feature is turned off. Select **Turn on** to enable Microsoft 365 Backup for your organization.

7. Review the applicable [terms of service for Microsoft 365 Backup](backup-preview-terms.md) and select **Confirm**.

    ![Screenshot of the Turn on Backup panel and the Confirm button.](../../media/content-understanding/backup-setup-turn-on.png)

8. Select **Go to Microsoft 365 Backup** to start setting up Microsoft 365 Backup on OneDrive, SharePoint, or Exchange.

    ![Screenshot of the Microsoft 365 Backup page showing SharePoint, Exchange, and OneDrive.](../../media/content-understanding/backup-setup-backup-page.png)

## Admin roles and backup management privileges

Only tenant-level admins can create and manage backups using Microsoft 365 Backup for their users. End users don't have the ability to enable backup or restores for their user account, distribution lists, mailboxes, or sites. It’s important to note that your admin role determines which products you can manage with Microsoft 365 Backup. In the future, we might introduce a Backup admin role that can control the entire tool.

|Admin role  |OneDrive  |SharePoint  |Exchange  |
|---------|---------|---------|---------|
|Global admin     | ✓        | ✓        | ✓       |
|SharePoint admin     | ✓        | ✓        |         |
|Exchange admin    |         |         | ✓        |

## Glossary

- **Protection units** – SharePoint sites, OneDrive accounts, or Exchange Online mailboxes backed up by the Microsoft 365 Backup tool.

- **Restore point** – A prior point in time from which you can restore a version of your content and metadata. If the protection unit from a prior point in time is identical to the present state of your data, then a restore from that point will have no impact on your current data.

- **RPO** – Recovery point objective, or how close in time the most recent restore point is to an impacting event.

- **RTO** – Recovery time objective, or how fast a restore to a prior point in time can complete.

## Set up backup policies for OneDrive, SharePoint, and Exchange

To use Microsoft 365 Backup for OneDrive, SharePoint, or Exchange, you need to create a backup policy for each product. A *policy* represents the backup plan defined by admins for protecting the Microsoft 365 data of an organization.

A policy contains details of what data (OneDrive accounts, SharePoint sites, and Exchange mailboxes) to protect. Although you see the retention period and backup frequency (which defines the restore point objective), those settings aren't currently variable or modifiable.

Select the **OneDrive**, **SharePoint**, or **Exchange** tab for steps to create a backup policy for that product.

# [OneDrive](#tab/onedrive)

Follow these steps to set up a backup policy for OneDrive accounts using Microsoft 365 Backup.

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home).

2. Select **Settings**.

3. Select **Microsoft 365 Backup** from the list of products.

4. On the **Microsoft 365 Backup** page, in the **OneDrive** section, select **Set up policy**.

    ![Screenshot of the Microsoft 365 Backup page with OneDrive highlighted.](../../media/content-understanding/backup-setup-backup-page-onedrive.png)

5. On the **Overview** page, review the backup features for OneDrive, and then select **Next**.

    ![Screenshot of the Overview page for OneDrive.](../../media/content-understanding/backup-overview-page-onedrive.png)

6. On the **Protection scope** page, you can set up OneDrive user accounts using any or all three ways. A protection scope is the scope of user accounts within OneDrive that you want to protect with Microsoft 365 Backup.

    ![Screenshot of the Protection scope page for OneDrive with the options highlighted.](../../media/content-understanding/backup-protection-scope-onedrive.png)

    a. Under **Add via search**, select **Choose accounts** to see user accounts that can be added via search. On the **Search and select accounts** panel, select the accounts you want to add to the policy.

    ![Screenshot of the Search and select accounts panel on the Protection scope page for OneDrive.](../../media/content-understanding/backup-protection-add-search-onedrive.png)

    b. Under **Add via**, select **Distribution lists** or **Security groups**, or both. The distribution list and security group are flattened when added, meaning the policy won't update dynamically if the groups or distribution list are updated later.

    ![Screenshot of the Add via Distribution lists and Security groups on the Protection scope page for OneDrive.](../../media/content-understanding/backup-protection-add-dl-sg-onedrive.png)

    c. Under **Import from file**, select **Upload CSV** to import user account details via CSV upload.

    ![Screenshot of the Import from file section on the Protection scope page for OneDrive.](../../media/content-understanding/backup-protection-import-file-onedrive.png)

8. On the **Review OneDrive backup policy** page, review the information to make sure it's how you want it, and then select **Create policy** (or **Update policy** if it's an update).

9. The backup policy for OneDrive is created.

    ![Screenshot of the OneDrive backup policy created page.](../../media/content-understanding/backup-policy-created-onedrive.png)

# [SharePoint](#tab/sharepoint)

Follow these steps to set up a backup policy for SharePoint sites using Microsoft 365 Backup.

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home).

2. Select **Settings**.

3. Select **Microsoft 365 Backup** from the list of products.

4. On the **Microsoft 365 Backup** page, in the **SharePoint** section, select **Set up policy**.

    ![Screenshot of the Microsoft 365 Backup page with SharePoint highlighted.](../../media/content-understanding/backup-setup-backup-page-sharepoint.png)

5. On the **Overview** page, review the backup features for SharePoint, and then select **Next**.

    ![Screenshot of the Overview page for SharePoint.](../../media/content-understanding/backup-overview-page-sharepoint.png)

6. On the **Protection scope** page, you can set up SharePoint sites by choosing to back up individual sites or collection of sites. A protection scope is the scope of sites within SharePoint that you want to protect with Microsoft 365 Backup.

    ![Screenshot of the Protection scope page for SharePoint with the options highlighted.](../../media/content-understanding/backup-protection-scope-sharepoint.png)

    a. Under **Add via search**, select **Choose sites** to see the individual sites or site collections that can be added via search. On the **Search and select sites** panel, select the sites you want to add to the policy.

    ![Screenshot of the Search and select sites panel on the Protection scope page for SharePoint.](../../media/content-understanding/backup-protection-add-search-sharepoint.png)

    b. Under **Add via**, select **Distribution lists** or **Security groups**, or both. The distribution list and security group are flattened when added, meaning the policy won't update dynamically if the groups or distribution list are updated later.

    c. Under **Import from file**, select **Upload CSV** to import user account details via CSV upload.

    ![Screenshot of the Import from file section on the Protection scope page for SharePoint.](../../media/content-understanding/backup-protection-import-file-sharepoint.png)

7. Once you've made the right selections, select **Next** to create the backup policy for SharePoint.

8. On the **Review SharePoint backup policy** page, review the information to make sure it's how you want it, and then select **Create policy** (or **Update policy** if it's an update).

    ![Screenshot of the Review SharePoint backup policy page.](../../media/content-understanding/backup-policy-review-policy-sharepoint.png)

9. The backup policy for SharePoint is created.

    ![Screenshot of the SharePoint backup policy created page.](../../media/content-understanding/backup-policy-created-sharepoint.png)

# [Exchange](#tab/exchange)

Follow these steps to set up a backup policy for Exchange mailboxes sites using Microsoft 365 Backup. Ensure that Microsoft 365 Backup is [enabled for your tenant](#enable-microsoft-365-backup).

1. Go to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home).

2. Select **Settings**.

3. Select **Microsoft 365 Backup** from the list of products.

4. On the **Microsoft 365 Backup** page, in the **Exchange** section, select **Set up policy**.

    ![Screenshot of the Microsoft 365 Backup page with Exchange highlighted.](../../media/content-understanding/backup-setup-backup-page-exchange.png)

5. On the **Overview** page, review and verify the backup policy attributes for Exchange, such as backup frequency, backup retention, cost details, and then select **Next**.

    ![Screenshot of the Overview page for Exchange.](../../media/content-understanding/backup-overview-page-exchange.png)

6. On the **Protection scope** page, choose the scope of protection for the mailbox policy. Microsoft 365 Backup for Exchange allows the addition of mailboxes in three ways.

    ![Screenshot of the Protection scope page for Exchange.](../../media/content-understanding/backup-protection-scope-exchange.png)

    a. Under **Add via search**, select **Choose user mailboxes** to see the mailboxes that can be added via search. On the **Search and select mailboxes** panel, select the mailboxes you want to add to the policy.

    ![Screenshot of the Search and select mailboxes panel on the Protection scope page for Exchange.](../../media/content-understanding/backup-protection-add-search-exchange.png)

    b. Under **Add via**, select **Distribution lists** or **Security groups**, or both. The distribution list and security group are flattened when added, meaning the policy won't update dynamically if the groups or distribution list are updated later.

    ![Screenshot of the Add via Distribution lists and Security groups on the Protection scope page for Exchange.](../../media/content-understanding/backup-protection-add-dl-sg-exchange.png)

    c. Under **Import from file**, select **Upload CSV** to import user account details via CSV upload.

    ![Screenshot of the Import from file section on the Protection scope page for Exchange.](../../media/content-understanding/backup-protection-import-file-exchange.png)

7. Once you've made the right selections, select **Next** to create the backup policy for Exchange.

8. On the **Review Exchange backup policy** page, review the information to make sure it's how you want it, and then select **Create policy** (or **Update policy** if it's an update).

    ![Screenshot of the Review Exchange backup policy page.](../../media/content-understanding/backup-policy-review-policy-exchange.png)

9. Wait for status of your policy to show as **Active** in the home screen. This might take between 15 and 60 minutes. The backup policy for Exchange is created. Select **View scope** at any time to verify the details.

    ![Screenshot of the Exchange backup policy created page.](../../media/content-understanding/backup-policy-created-exchange.png)

---
