---
title: Configuration Manager PowerShell cmdlets
description: Manage your Configuration Manager hierarchy using Windows PowerShell. 
ms.date: 11/20/2020
ms.prod: configuration-manager
ms.technology: configmgr-sdk
ms.topic: overview
ms.assetid: 63712bbf-0f8a-4cdb-8998-e7d41257981e
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get started with Configuration Manager cmdlets

*Applies to: Configuration Manager (current branch)*

Use Windows PowerShell to manage your Configuration Manager hierarchy. You can use PowerShell scripts to automate or extend Configuration Manager similar to other documented approaches using WMI and C#. For more information, see [Configuration Manager SDK](/mem/configmgr/develop/).

Run Configuration Manager cmdlets and scripts in PowerShell from the Configuration Manager console or from a Windows PowerShell session. When you run Configuration Manager cmdlets by using the Configuration Manager console, your session automatically runs in the context of the site.

> [!NOTE]
> All currently supported versions of Configuration Manager current branch support Windows PowerShell version 5.1. If you've already installed PowerShell version 7, you can still use PowerShell version 5.1. For more information, see [Using PowerShell 7 side-by-side with Windows PowerShell 5.1](/powershell/scripting/install/migrating-from-windows-powershell-51-to-powershell-7#using-powershell-7-side-by-side-with-windows-powershell-51).
>
> Starting in version 2010, the Configuration Manager PowerShell cmdlet library supports PowerShell 7. For more information, see [Support for PowerShell version 7](#support-for-powershell-version-7).<!--6023299-->

## PowerShell from the Configuration Manager console

The easiest method to open PowerShell is directly from the Configuration Manager console.

1. Launch the Configuration Manager console. In the upper-left corner, there's a blue rectangle. Select the white arrow in the blue rectangle, and choose **Connect via Windows PowerShell**.

1. After Windows PowerShell loads, you'll see a prompt that contains your site code. For example, if the site code is "ABC", the prompt looks like: `PS ABC:\>`

1. To verify it works, use the **Get-CMSite** cmdlet. This cmdlet returns information about the Configuration Manager site you're currently connected to and any child sites. For example, the site server name, installation director, site name, and version.

## Import the Configuration Manager PowerShell module

Connect to Configuration Manager from an existing Windows PowerShell session by manually loading the Configuration Manager module.

1. Open a Windows PowerShell session from the Start menu.

1. Import the Configuration Manager module by using the **Import-Module** cmdlet. Specify the path to the Configuration Manager module, or change to the directory that contains the module. By default, the module is at the following path: `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\ConfigurationManager.psd1`

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
    > You can also use the **SMS_ADMIN_UI_PATH** environment variable. For example:
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

1. Confirm that PowerShell properly loaded the Configuration Manager module by using the **Get-CMSite** cmdlet.

## Update help

Update Windows PowerShell help by using the **Update-Help** cmdlet. This action can also update the help for the Configuration Manager cmdlets. If your computer is connected to the internet, go to your Windows PowerShell window, and type the following command:

```powershell
Update-Help –Module ConfigurationManager
```

After you update the Configuration Manager cmdlet help, you can get help about the cmdlets by using the **Get-Help** cmdlet. For example:

```powershell
Get-Help Get-CMSite
```

## Support for PowerShell version 7

<!--6023299-->

Starting in version 2010, the Configuration Manager PowerShell cmdlet library supports PowerShell version 7. For more information on PowerShell 7, including directions on how to download and install it, see [Install PowerShell on Windows](/powershell/scripting/install/installing-powershell-core-on-windows).

> [!TIP]
> PowerShell 7 runs as `pwsh.exe`. Earlier versions of PowerShell run as `powershell.exe`.

### Known issues with PowerShell version 7

- You can't launch PowerShell 7 directly from the Configuration Manager console. Manually start PowerShell 7, and then [import the Configuration Manager module](#import-the-configuration-manager-powershell-module).

- Configuration Manager cmdlets with **Import-** and **Export-** verbs may not function as expected.

- Current support is only for the Configuration Manager cmdlets. Other features of Configuration Manager that rely on PowerShell may not support version 7. For example, [Run Scripts](/mem/configmgr/apps/deploy-use/create-deploy-scripts), [CMPivot](/mem/configmgr/core/servers/manage/cmpivot), or the [Run PowerShell Script](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RunPowerShellScript) task sequence step.

## Feedback for PowerShell

If you have feedback on the Configuration Manager PowerShell cmdlets, use the same options in the Configuration Manager console to send feedback. For more information, see [Product feedback](/mem/configmgr/core/understand/product-feedback).

When you send a frown, include the following additional information specific to PowerShell:

- The exact script or command syntax that you used so that Microsoft can try to reproduce the issue.

- What behavior you expected compared to the actual behavior.

- The full output when you run it with the [Verbose](/powershell/module/microsoft.powershell.core/about/about_commonparameters#verbose) common parameter.

- The version and path of the **ConfigurationManager** module. For example, include the output of the following commands:

    ```powershell
    (Get-Module -Name ConfigurationManager).Version
    (Get-Module -Name ConfigurationManager).Path
    ```

- If a cmdlet returns an error, use the following command to get exception details:

    ```powershell
    $Error[0].Exception | Format-List * -Force
    ```

## Next steps

For more information about what's changed in the most recent release of Configuration Manager, select the latest **Release Notes** from the table of contents.

For more information on individual cmdlets, see the [Configuration Manager cmdlet reference](/powershell/module/configurationmanager/).

For more information on learning and getting started with Windows PowerShell, see [PowerShell 101](/powershell/scripting/learn/ps101/00-introduction).
