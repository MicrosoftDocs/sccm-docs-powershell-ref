---
description: Create bootable media.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMBootableMedia
---

# New-CMBootableMedia

## SYNOPSIS

Create bootable media.

## SYNTAX

```
New-CMBootableMedia [-AllowUacPrompt] [-AllowUnattended] [-AllowUnknownMachine] -BootImage <IResultObject>
 [-CertificateExpireTime <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-CertificateStartTime <DateTime>] -DistributionPoint <IResultObject[]> [-Force] [-FormatMedia]
 -ManagementPoint <IResultObject[]> [-SiteCode <String>] -MediaMode <MediaMode> [-MediaPassword <SecureString>]
 -MediaType <MediaInputType> [-NoAutoRun] -Path <String> [-PrestartCommand <String>]
 [-PrestartPackage <IResultObject>] [-TemporaryFolder <String>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-Variable <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates media used to deploy an OS. Bootable media contains the boot image, optional prestart commands and associated files, and Configuration Manager files. Use bootable media to install a new version of Windows on a new computer (bare metal), or to replace an existing computer and transfer settings.

> [!NOTE]
> This cmdlet requires elevated permissions to run.

For more information, see [Task sequence media overview](/mem/configmgr/osd/deploy-use/create-task-sequence-media).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create bootable media

The first command gets the boot image object named **Boot image (x64)** and stores it in the **$BootImage** variable. The second command gets the distribution point role for  **SiteServer01.Contoso.com** and stores it in the **$DistributionPoint** variable. The third command gets the management point role for **SiteServer02.Contoso.com** and stores it in the **$ManagementPoint** variable. The last command creates bootable media in dynamic mode. It uses the objects stored in the previous variables.

```powershell
$BootImage = Get-CMBootImage -Name "Boot image (x64)"
$DistributionPoint = Get-CMDistributionPoint -SiteCode CM1
$ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "SiteSystemServer02.Contoso.com"

New-CMBootableMedia -MediaMode Dynamic -MediaType CdDvd -Path "\\Server\share\test.iso" -AllowUnknownMachine -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint
```

## PARAMETERS

### -AllowUacPrompt

Add this parameter to allow Windows to prompt you to elevate your administrator permissions with User Account Control (UAC). This cmdlet requires elevated permissions to run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUnattended

Add this parameter to allow an unattended OS deployment. An unattended OS deployment doesn't prompt for network configuration or optional task sequences.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUnknownMachine

Add this parameter to allow Configuration Manager to provision unknown computers. An unknown computer is a computer that the site hasn't discovered yet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImage

Specify a boot image object. To get this object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: BootImagePackage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpireTime

If you create a self-signed media certificate for HTTP communication, this parameter specifies the certificate's expiration date and time. Specify a datetime sufficiently in the future. When this certificate expires, you can't use the bootable media. Use the **-CertificateStartTime** parameter to set the start date.

For example:

```powershell
$date = [datetime]::parseexact("11/16/2021", 'MM/dd/yyyy', $null)
```

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword

If you use the **-CertificatePath** parameter to import a PKI certificate for HTTPS communication, use this parameter to specify the password for the certificate file.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath

Specify the path to a PKI certificate to import. Use the **-CertificatePassword** parameter to specify the password for this certificate file. Use these parameters if you configure the site for HTTPS client communication.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateStartTime

To create a self-signed certificate for HTTP communication, this parameter specifies the certificate's start date and time. Use the **-CertificateExpireTime** parameter to set the expiration date. You can't use the bootable media until this date.

For example:

```powershell
$date = [datetime]::parseexact("11/16/2020", 'MM/dd/yyyy', $null)
```

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPoint

Specify one or more distribution point objects to which you distributed the boot image. To get this object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DistributionPoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FormatMedia

If the **MediaType** is `Usb`, you can add this parameter to format the removable USB drive as FAT32, and make it bootable.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementPoint

Specify one or more management point objects that the media uses in initial communication. Use the **-MediaMode** parameter to determine how the media communicates when it runs. To get this object, use the [Get-CMManagementPoint](Get-CMManagementPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: ManagementPoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaMode

Specify how the client finds a management point to get deployment information:

- `Dynamic`: The media contacts a management point, which redirects the client to a different management point based on the client location in the site boundaries.

- `SiteBased`: The media communicates the management point specified with the **-ManagementPoint** parameter.

```yaml
Type: MediaMode
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, SiteBased

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaPassword

Specify a secure string password to protect the task sequence media. When you boot a device with this media, you have to enter the password to continue.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaType

Specify whether the media is a CD/DVD set or a removable USB drive.

```yaml
Type: MediaInputType
Parameter Sets: (All)
Aliases:
Accepted values: Usb, CdDvd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoAutoRun

Add this parameter to include the autorun.inf file on the media. Configuration Manager doesn't add it by default. This file is commonly blocked by antimalware products. For more information on the AutoRun feature of Windows, see [Creating an AutoRun-enabled CD-ROM Application](/windows/desktop/shell/autoplay). If still necessary for your scenario, add this parameter to include the file.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

If the **MediaType** is `CdDvd`, specify the name and path where Configuration Manager writes the output files. For example, `C:\output\boot.iso`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MediaPath, OutputPath, DriveName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartCommand

Specify a prestart command that runs before the task sequence. A prestart command is a script or an executable that can interact with the user in Windows PE before the task sequence runs to install the OS. If the command isn't native to Windows PE, use the **PrestartPackage** to include files for the command.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PreExecCommandLine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartPackage

If you use the **PrestartCommand** parameter, use this parameter to specify a package that contains files for the prestart command. To get the package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode

Applies to version 2010 and later. Use this parameter with the **ManagementPoint** parameter to specify the site code.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemporaryFolder

The media creation process can require much temporary drive space. By default, Configuration Manager uses the temporary directory of the current user: `$env:temp`. For example, `C:\Users\jqpublic\AppData\Local\Temp\`. To give you greater flexibility with where to store these temporary files, specify a custom location for staging temporary data.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TemporaryDirectory, StagingArea

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeviceAffinity

To support user-centric management in Configuration Manager, specify how you want the media to associate users with the destination computer. For more information about how OS deployment supports user device affinity, see [Associate users with a destination computer](/mem/configmgr/osd/get-started/associate-users-with-a-destination-computer).

- `DoNotAllow`: Don't allow user device affinity. The media doesn't associate users with the destination computer. In this scenario, the task sequence doesn't associate users with the destination computer when it deploys the OS.

- `AdministratorApproval`: Allow user device affinity pending administrator approval. The media associates users with the destination computer after you grant approval. This functionality is based on the scope of the task sequence that deploys the OS. In this scenario, the task sequence creates a relationship between the specified users and the destination computer. It then waits for approval from an administrative user before it deploys the OS.

- `AutoApproval`: Allow user device affinity with auto-approval. The media automatically associates users with the destination computer. This functionality is based on the actions of the task sequence that deploys the OS. In this scenario, the task sequence creates a relationship between the specified users and destination computer when it deploys the OS to the destination computer.

```yaml
Type: UserDeviceAffinityType
Parameter Sets: (All)
Aliases:
Accepted values: DoNotAllow, AdministratorApproval, AutoApproval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable

Specify one or more task sequence variables and values in a hashtable. A task sequence variable is a name/value pair that is used during the task sequence deployment.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: TaskSequenceVariables, Variables

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMPackage](Get-CMPackage.md)

[New-CMPrestageMedia](New-CMPrestageMedia.md)
[New-CMCaptureMedia](New-CMCaptureMedia.md)
[New-CMStandaloneMedia](New-CMStandaloneMedia.md)
