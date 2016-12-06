---
ms.assetid:
ms.title: Get started with SCCM cmdlets | Microsoft Docs
ms.prod: "configuration-manager"
ms.service:
author: "shill-ms"
ms.author: "v-suhill"
ms.manager: "mbaldwin"
---

# Get started with Microsoft System Center Configuration Manager cmdlets
In System Center Configuration Manager, Windows PowerShell allows you to manage a Configuration Manager hierarchy by using Windows PowerShell scripts, Windows PowerShell cmdlets, and the Windows PowerShell Drive Provider.

The basic method of accessing Configuration Manager functionality is through the SMS Provider (WMI). Building PowerShell scripts to automate or extend Configuration Manager is similar to earlier documented approaches using VBScript and C#.

## Using the Configuration Manager PowerShell cmdlets
You can run Configuration Manager cmdlets and scripts by using the Configuration Manager console or by using a Windows PowerShell session. When you run Configuration Manager cmdlets by using the Configuration Manager console, your session runs in the context of the site.

### Load Windows PowerShell from the Configuration Manager Console
The easiest method to load Windows PowerShell is directly from the Configuration Manager console.  

1.  Start by launching the Configuration Manager console. In the upper left corner, there’s a blue rectangle. Click the white arrow in the blue rectangle, and choose **Connect via Windows PowerShell**.

2.  After Windows PowerShell loads, you’ll see a prompt that contains your site code. For example, if the site code is "ABC", the prompt looks like:

    ```  
    PS ABC:\>  
    ```  

3.  Let's verify everything is working by using the **Get-CMSite** cmdlet. This cmdlet will return information about the Configuration Manager site you're currently connected to.

    Go to your Windows PowerShell window, and type in `Get-CMSite`. You should see the following output (with your site information) in your Windows PowerShell window:

    ```  
    PS ABC:\> get-cmsite  

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

### Import the Configuration Manager PowerShell Module
Another method of connecting to Configuration Manager from your Windows PowerShell environment is to load the Configuration Manager module manually.  

1.  Right-click the Windows PowerShell icon and choose "Run as administrator".

    You should now see your PowerShell environment.

    ```  
    Windows PowerShell  
    Copyright (C) 2016 Microsoft Corporation. All rights reserved.  

    PS C:\WINDOWS\system32>  
    ```

2.  Now, you need to import the Configuration Manager module by using the Windows PowerShell **Import-Module** cmdlet. To import the Configuration Manager module, you will have to specify the path to the Configuration Manager module or change to the directory that contains the module. Here, we're going to change to the module's directory.

    Go to your Windows PowerShell window, and type in `CD 'C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin'`:  

    ```  
    PS C:\>  
    PS C:\> CD 'C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin'  
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin>  

    ```  

    Go to your Windows PowerShell window, and type in `Import-Module .\ConfigurationManager.psd1`:  

    ```  
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin>  
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin> Import-Module .\ConfigurationManager.psd1  
    ```  

 > [!NOTE]
 > To run the Configuration Manager cmdlets, you need to switch the path to the Configuration Manager site.

3.  Go to your Windows PowerShell window, and type in CD \<site code\>:, replacing \<site code\> with your site code (the site code "ABC" is used below):

    ```  
    PS C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin> CD ABC:   
    PS ABC:\>  
    ```

4.  Confirm that the Configuration Manager module has been loaded by using the **Get-CMSite** cmdlet.

    Go to your Windows PowerShell window, and type in `Get-CMSite`.

5.  If you see the following output (with your site information), you are connected to the Configuration Manager site and the Configuration Manager module is loaded.

    ```  
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

## Update Help

1.  You can update Windows PowerShell help (and specifically the help for the Configuration Manager cmdlets) by using the Update-Help cmdlet. If your computer is connected to the Internet, go to your Windows PowerShell window, and type in `Update-Help –Module configurationmanager`. Ensure that you are running Windows PowerShell as Administrator.

2.  After you have installed the Configuration Manager cmdlet help, you can get help about the cmdlets by using the **Get-Help** cmdlet. For example, go to your Windows PowerShell window, and type in `Get-Help Get-CMSite`.
