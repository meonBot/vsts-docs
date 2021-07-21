---
title: Share your Azure Artifacts packages with badges
description: Share your NuGet, npm, Maven, Python, or Universal Packages with package badges
ms.assetid: 60a3f33a-d8bc-436a-a676-c1bd4b3066e7
ms.technology: devops-artifacts
ms.topic: conceptual
ms.date: 06/01/2021
monikerRange: '>= tfs-2018'
---

# Share your Artifacts with package badges

**Azure DevOps Services | Azure DevOps Server 2020 | Azure DevOps Server 2019 | TFS 2018**

Azure Artifacts offers a way to share your packages anywhere you can share an image by using package badges. You can embed package badges directly into your project's home page or in any Markdown file so your customers can easily discover and consume your packages.

:::image type="content" source="media/package-badge.png" alt-text="NuGet package badge":::
 
> [!NOTE]
> Package badges can only be created and shared for released versions. Pre-released packages will not be displayed in badges, instead the badge will show the latest release version.

## Enable package sharing  

To start sharing your Artifacts packages using package badges, you'll first have to enable **Package sharing** for you feed.

> [!NOTE]
> Only feed administrators can enable package sharing.

1. From within your project, select **Artifacts**, and then select the gear icon ![gear icon](../media/icons/gear-icon.png) then select **Feed settings** from the dropdown menu. 

   ::: moniker range=">= azure-devops-2019"

   :::image type="content" source="media/edit-feed-full-newnav.png" alt-text="Feed settings":::

   ::: moniker-end

   ::: moniker range="<= tfs-2018"

   :::image type="content" source="media/edit-feed-full.png" alt-text="Feed settings TFS":::

   ::: moniker-end

1. Find the **Package sharing** section and select the checkbox to **Enable package badges**.

   :::image type="content" source="media\enable-package-badges.png" alt-text="Enable package badges":::

    ::: moniker range=">= azure-devops-2019"

    This will enable the **Create badge** button for every package in that feed.

    :::image type="content" source="media/pm-create-badge-newnav.png" alt-text="Create a package badge":::

    ::: moniker-end

    ::: moniker range="<= tfs-2018"

    This will enable the **Create badge** button for every package in that feed.

    :::image type="content" source="media/pm-create-badge.png" alt-text="Create a package badge TFS":::

    ::: moniker-end

## Create badge

You can create a badge for any package in your feed with package-sharing enabled. You can only create a badge for the latest version of each package.

1. From within your feed, select your package and then select the **Create badge** button. 

    :::image type="content" source="media/create-badge.png" alt-text="Create a package for a specific package":::

1. Select a **Feed view** for your package badge. If you're using release views, select the view that contains the packages you want to share; otherwise, just use *No view*.

    :::image type="content" source="media/package-badge-setup.png" alt-text="package badge configuration":::

1. You can now share your package by using the markdown snippet or the direct image link.

## Related articles

- [Limits of package sizes and counts](./reference/limits.md)
- [Package alerts](./how-to/follow-package-notifications.md)
- [Use public feeds to share your packages](./tutorials/share-packages-publicly.md)