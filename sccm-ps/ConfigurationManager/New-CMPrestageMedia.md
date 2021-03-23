---
description: Create an OS deployment prestaged media file.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMPrestageMedia
---

# New-CMPrestageMedia

## SYNOPSIS

Create an OS deployment prestaged media file.

## SYNTAX

```
New-CMPrestageMedia [-Application <IResultObject[]>] [-Comment <String>] [-CreatedBy <String>]
 [-DriverPackage <IResultObject[]>] [-IncludeApplicationDependency] -OperatingSystemImage <IResultObject>
 [-OperatingSystemImageIndex <Int32>] [-Package <IResultObject[]>] -TaskSequence <IResultObject>
 [-Version <String>] [-AllowUacPrompt] [-AllowUnattended] [-AllowUnknownMachine] -BootImage <IResultObject>
 [-CertificateExpireTime <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-CertificateStartTime <DateTime>] -DistributionPoint <IResultObject[]> [-Force]
 -ManagementPoint <IResultObject[]> [-SiteCode <String>] -MediaMode <MediaMode> [-MediaPassword <SecureString>]
 [-NoAutoRun] -Path <String> [-PrestartCommand <String>] [-PrestartPackage <IResultObject>]
 [-TemporaryFolder <String>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMPrestageMedia** cmdlet creates a file to prestage an OS image on a new hard drive. For more information, see [Plan prestaged media](/mem/configmgr/osd/deploy-use/create-task-sequence-media#BKMK_PlanPrestagedMedia).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create prestaged media

The first command gets the management point object for the site system server named **mp01.contoso.com** in the site code **CM1** and stores the object in the **$ManagementPoint** variable.

The second command gets the boot image object named **BootImage01** and stores the object in the **$BootImage** variable.

The third command gets the distribution point object for the site system server named **dist01.contoso.com** in the site code **CM1** and stores the object in the **$DistributionPoint** variable.

The fourth command gets the OS image object named **OSImagePkg01** and stores the object in the **$OSImage** variable.

The last command creates a dynamic prestaged media file named **PrestagedMedia.wim** with the boot image stored in **$BootImage**, the distribution point stored in **$DistributionPoint**, the management point stored in **$ManagementPoint**, and the OS image stored in $OSImage.

```powershell
$ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "mp01.contoso.com" -SiteCode "CM1"
$BootImage = Get-CMBootImage -Name "BootImage01"
$DistributionPoint = Get-CMDistributionPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
$OSImage = Get-CMOperatingSystemImage -Name "OSImagePkg01"

New-CMPrestageMedia -MediaMode Dynamic -Path "\\server\share\PrestagedMedia.wim" -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint -OperatingSystemImage $OSImage
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

### -Application

Specify an array of application objects to include as part of the media file. If the task sequence references this content, it first looks locally for the content. If the content isn't in the media, the task sequence tries to download it from the network as normal. To get an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Applications

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



$date = [datetime]::parseexact("11/16/2021", 'MM/dd/yyyy', $null)

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



$date = [datetime]::parseexact("11/16/2020", 'MM/dd/yyyy', $null)

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

### -Comment

An optional string to provide further details about the media. It's useful to describe how you configured or how you'll use this media. The maximum length is 127 characters.

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

### -CreatedBy

An optional string to specify who created this media, which is useful for tracking purposes. The maximum length is 50 characters.

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

Specify one or more distribution point objects to which you distributed the content for this media. To get this object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

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

### -DriverPackage

Specify an array of driver package objects to include as part of the media file. If the task sequence references this content, it looks locally for the content. If the content isn't in the media, the task sequence tries to download it from the network as normal. To get this object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DriverPackages, PackageDriver, PackageDrivers

Required: False
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

### -IncludeApplicationDependency

Add this parameter to detect associated application dependencies and add them to this media.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: IncludeApplicationDependencies

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

### -OperatingSystemImage

Specify an OS image package object to include for this media. Use the **OperatingSystemImageIndex** parameter to specify the image index in the image package. To get this object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: OperatingSystemImagePackage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageIndex

Specify the image index in the image package from the **OperatingSystemImage** parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package

Specify an array of package objects to include in the media file. If the task sequence references this content, it looks locally for the content. If the content isn't in the media, the task sequence tries to download it from the network as normal. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Packages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

The path to the media file to create. The format is either a drive/directory path or a valid network path. For example:

- `C:\media\prestaged1.wim`
- `\\server\share\prestaged1.wim`

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

Specify a command line to run before the task sequence starts. For more information, see [Prestart commands for task sequence media](/mem/configmgr/osd/understand/prestart-commands-for-task-sequence-media).

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

If you specify a **PrestartCommand**, use this parameter to specify a package for prestart content if needed.

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

### -TaskSequence

Specify a task sequence object for this media to run. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
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

Specify a hashtable of task sequence variables to use during the task sequence deployment from this media.

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

### -Version

An optional string value to specify a version for this media, which is useful for tracking and revision purposes. The maximum length is 32 characters.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
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

Cmdlet aliases: **New-CMPrestagedMedia**

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMPackage](Get-CMPackage.md)

[Plan prestaged media](/mem/configmgr/osd/deploy-use/create-task-sequence-media#BKMK_PlanPrestagedMedia)
