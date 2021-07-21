---
ms.topic: include
ms.technology: devops-cicd
ms.author: rabououn
author: ramiMSFT
ms.date: 07/15/2021
---

::: moniker range=">= azure-devops-2019"

1. From within your project, select **Artifacts**, and then select your feed. You can [create a new feed](../../get-started-nuget.md#create-a-feed) if you don't have one already. 

1. Select **Connect to feed**.

    :::image type="content" source="../../media/connect-to-feed-azure-devops-newnav.png" alt-text="Connect to your feed":::

1. Select **NuGet.exe** under the **NuGet** header.

    :::image type="content" source="../../media/nuget-connect-feed.png" alt-text="NuGet.exe feed connection":::

1. If this is the first time using Azure Artifacts with Nuget.exe, select **Get the tools** button and follow the instructions to install the prerequisites.

    1. Download the [latest NuGet version](https://www.nuget.org/downloads).
    1. Download and install the [Azure Artifacts Credential Provider](https://github.com/microsoft/artifacts-credprovider#azure-artifacts-credential-provider).

1. Follow the instructions in the **Project setup** to connect to your feed. 

    :::image type="content" source="../../media/project-setup.png" alt-text="Project setup":::

## Publish a NuGet package by using the command line

If you don't have a NuGet package but you want to try publishing your package to your feed, you can install the *HelloWorld* sample package.

```Command
nuget install HelloWorld -ExcludeVersion
```

Run the following command to publish your package to your feed:

```Command
nuget.exe push -Source "<YOUR_FEED_NAME>" -ApiKey <ANY_STRING> <PACKAGE_PATH>
```

::: moniker-end

::: moniker range=">=tfs-2017 < azure-devops-2019"

1. Select **Build and Release** > **Packages**.

1. Select your feed from the dropdown menu or [create one](../../get-started-nuget.md#create-a-feed) if you haven't. 

1. Select **Connect to feed**.

    :::image type="content" source="../../media/connect-to-feed.png" alt-text="Connect to feed - TFS":::

1. Select **NuGet** and follow the instruction to connect to your feed.

    :::image type="content" source="../../media/connect-to-nuget-feed-tfs.png" alt-text="Connect to NuGet feed - TFS":::

::: moniker-end