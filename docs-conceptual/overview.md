---
title: Get started with ConfigMgr cmdlets
titleSuffix: Configuration Manager
description: Manage your Configuration Manager hierarchy using Windows PowerShell. 
ms.date: 09/19/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.assetid: 63712bbf-0f8a-4cdb-8998-e7d41257981e
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get started with Configuration Manager cmdlets

*Applies to: System Center Configuration Manager (Current Branch)*

Use Windows PowerShell to manage your Configuration Manager hierarchy with scripts, cmdlets, and the drive provider.

The basic method of accessing Configuration Manager functionality is through the SMS Provider (WMI). Building PowerShell scripts to automate or extend Configuration Manager is similar to other documented approaches using VBScript and C#. For more information, see [Configuration Manager SDK](https://docs.microsoft.com/sccm/develop/core/misc/system-center-configuration-manager-sdk).



## Using the Configuration Manager cmdlets

Run Configuration Manager cmdlets and scripts by using the Configuration Manager console or by using a Windows PowerShell session. When you run Configuration Manager cmdlets by using the Configuration Manager console, your session runs in the context of the site.


### Load Windows PowerShell from the Configuration Manager console

The easiest method to load Windows PowerShell is directly from the Configuration Manager console.  

1.  Start by launching the Configuration Manager console. In the upper-left corner, there's a blue rectangle. Select the white arrow in the blue rectangle, and choose **Connect via Windows PowerShell**.  

2.  After Windows PowerShell loads, you'll see a prompt that contains your site code. For example, if the site code is "ABC", the prompt looks like:  

    ```  PowerShell
    PS ABC:\>  
    ```  

3.  First verify everything is working by using the `Get-CMSite` cmdlet. This cmdlet returns information about the Configuration Manager site you're currently connected to. In your Windows PowerShell window you should see output similar to the following example:  

    ```  PowerShell
    PS ABC:\> Get-CMSite  

    BuildNumber       : 7958  
    Features          : 0000000000000000000000000000000000000000000000000000000000000000  
    InstallDir        : C:\Program Files\Microsoft Configuration Manager  
    Mode              : 0  
    ReportingSiteCode :  
    RequestedStatus   : 110  
    ServerName        : SDKTESTLAB.test.lab  
    SiteCode          : ABC  
    SiteName          : ABC Test Site  
    Status            : 1  
    TimeZoneInfo      : 000001E0 0000 000B 0000 0001 0002 0000 0000 0000 00000000 0000 0003 0000 0002 0002 0000 0000 0000  
                        FFFFFFC4  
    Type              : 2  
    Version           : 5.00.7958.1000  

    ```  


### Import the Configuration Manager PowerShell module

Another method of connecting to Configuration Manager from your Windows PowerShell environment is to load the Configuration Manager module manually.  

1.  Right-click the Windows PowerShell icon and choose "Run as administrator".  

2.  Import the Configuration Manager module by using the `Import-Module` cmdlet. To import the Configuration Manager module, specify the path to the Configuration Manager module, or change to the directory that contains the module. By default, the module is at the following path: `C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin\ConfigurationManager.psd1`   

    The following example changes to the module's directory and then imports it:  

    ```  PowerShell
    PS C:\>  
    PS C:\> CD 'C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin'  
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin> Import-Module .\ConfigurationManager.psd1  
    ```  

3.  To run the Configuration Manager cmdlets, you need to switch the path to the Configuration Manager site. In the following example, the site code is `ABC`:  

    ```  PowerShell
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin> CD ABC:   
    PS ABC:\>  
    ```  

4.  Confirm that PowerShell properly loaded the Configuration Manager module by using the `Get-CMSite` cmdlet.  



## Update help

Update Windows PowerShell help by using the `Update-Help` cmdlet. This action can also update the help for the Configuration Manager cmdlets. If your computer is connected to the internet, go to your Windows PowerShell window, and type in `Update-Help –Module configurationmanager`. Make sure that you're running Windows PowerShell as an administrator.  

After you have installed the Configuration Manager cmdlet help, you can get help about the cmdlets by using the `Get-Help` cmdlet. For example, go to your Windows PowerShell window, and type in `Get-Help Get-CMSite`.


## Next steps

For more information about what's changed in the most recent release of Configuration Manager, select the latest **Release Notes** from the table of contents to the left. 

For more information on individual cmdlets, see the [Configuration Manager cmdlet reference](https://docs.microsoft.com/powershell/module/configurationmanager/?view=sccm-ps).

