---
title: Configuration Manager PowerShell cmdlets
description: Manage your Configuration Manager hierarchy using Windows PowerShell. 
ms.date: 07/14/2020
ms.prod: configuration-manager
ms.technology: configmgr-sdk
ms.topic: conceptual
ms.assetid: 63712bbf-0f8a-4cdb-8998-e7d41257981e
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get started with Configuration Manager cmdlets

*Applies to: Configuration Manager (current branch)*

Use Windows PowerShell to manage your Configuration Manager hierarchy. You can use PowerShell scripts to automate or extend Configuration Manager similar to other documented approaches using WMI and C#. For more information, see [Configuration Manager SDK](https://docs.microsoft.com/mem/configmgr/develop/).

Run Configuration Manager cmdlets and scripts in PowerShell from the Configuration Manager console or from a Windows PowerShell session. When you run Configuration Manager cmdlets by using the Configuration Manager console, your session automatically runs in the context of the site.

## PowerShell from the Configuration Manager console

The easiest method to open PowerShell is directly from the Configuration Manager console.

1. Launch the Configuration Manager console. In the upper-left corner, there's a blue rectangle. Select the white arrow in the blue rectangle, and choose **Connect via Windows PowerShell**.

    :::image type="content" source="./media/console-menu.png" alt-text="Menu in Configuration Manager console with PowerShell option":::

1. After Windows PowerShell loads, you'll see a prompt that contains your site code. For example, if the site code is "ABC", the prompt looks like: `PS ABC:\>`

1. To verify it works, use the `Get-CMSite` cmdlet. This cmdlet returns information about the Configuration Manager site you're currently connected to and any child sites. For example, the site server name, installation director, site name, and version.

## Import the Configuration Manager PowerShell module

Connect to Configuration Manager from an existing Windows PowerShell session by manually loading the Configuration Manager module.

1. Open a Windows PowerShell session from the Start menu.

1. Import the Configuration Manager module by using the `Import-Module` cmdlet. Specify the path to the Configuration Manager module, or change to the directory that contains the module. By default, the module is at the following path: `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\ConfigurationManager.psd1`

    > [!IMPORTANT]
    > This path changed starting in version 1910 to use the `Microsoft Endpoint Manager` folder. Make sure you don't import an older version of the module that might exist in another folder. After you import the module, use the following commands to check the module version and path:
    >
    > ```powershell
    > (Get-Module -Name ConfigurationManager).Version
    > (Get-Module -Name ConfigurationManager).Path
    > ```

    The following example changes to the module's directory and then imports it:

    ```PowerShell
    Set-Location 'C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin'
    Import-Module .\ConfigurationManager.psd1
    ```

    > [!TIP]
    > You can also use the `$env:SMS_ADMIN_UI_PATH` variable. For example:
    >
    > ```powershell
    > Set-Location $env:SMS_ADMIN_UI_PATH\..\
    > ```
    >
    > Also, you can use the **cd** alias to change directories instead of the **Set-Location** cmdlet.

1. If it's the first time importing the Configuration Manager module on this computer, you may need to create the site drive.<!-- SCCMDocs#1915 --> For example:

    ```powershell
    New-PSDrive -Name "ABC" -PSProvider "AdminUI.PS.Provider\CMSite" -Root "siteserver.contoso.com" -Description "Primary site"
    ```

    > [!TIP]
    > When you start PowerShell from the console, it automatically creates the PSDrive as a convenience for the currently connected site. If you're in a hierarchy, use **New-PSDrive** to create drives for each site.

1. To run the Configuration Manager cmdlets, you need to switch the path to the Configuration Manager site. In the following example, the site code is `ABC`:

    ```powershell
    Set-Location ABC:
    ```

1. Confirm that PowerShell properly loaded the Configuration Manager module by using the `Get-CMSite` cmdlet.

## Update help

Update Windows PowerShell help by using the `Update-Help` cmdlet. This action can also update the help for the Configuration Manager cmdlets. If your computer is connected to the internet, go to your Windows PowerShell window, and type the following command:

```powershell
Update-Help –Module ConfigurationManager
```

After you update the Configuration Manager cmdlet help, you can get help about the cmdlets by using the `Get-Help` cmdlet. For example:

```powershell
Get-Help Get-CMSite
```

## Next steps

For more information about what's changed in the most recent release of Configuration Manager, select the latest **Release Notes** from the table of contents.

For more information on individual cmdlets, see the [Configuration Manager cmdlet reference](https://docs.microsoft.com/powershell/module/configurationmanager/?view=sccm-ps).

For more information on learning and getting started with Windows PowerShell, see [PowerShell 101](https://docs.microsoft.com/powershell/scripting/learn/ps101/00-introduction?view=powershell-7).
