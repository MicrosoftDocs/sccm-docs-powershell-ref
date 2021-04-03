---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/30/2021
schema: 2.0.0
title: New-CMTaskSequence
---

# New-CMTaskSequence

## SYNOPSIS

Create a task sequence.

## SYNTAX

### NewBuildOSImage (Default)
```
New-CMTaskSequence [-ApplicationName <String[]>] [-ApplyAll <Boolean>] -BootImagePackageId <String>
 [-BuildOperatingSystemImage] [-ClientPackagePackageId <String>] [-CreatedBy <String>] [-Description <String>]
 [-DomainAccount <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainPassword <SecureString>] [-GeneratePassword <Boolean>] [-HighPerformance <Boolean>]
 [-IgnoreInvalidApplication <Boolean>] [-ImageDescription <String>] [-ImageVersion <String>]
 [-InstallationLicensingMode <ServerLicensingMode>] [-InstallationProperty <String>] -JoinDomain <JoinType>
 [-LocalAdminPassword <SecureString>] [-MaximumServerConnection <Int32>] -Name <String>
 -OperatingSystemFileAccount <String> [-OperatingSystemFileAccountPassword <SecureString>]
 -OperatingSystemFilePath <String> -OperatingSystemImageIndex <UInt32> -OperatingSystemImagePackageId <String>
 [-ProductKey <String>] [-SoftwareUpdateStyle <SoftwareUpdateStyleType>] [-TimeZone <TimeZoneInfo>]
 [-WorkgroupName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewInstallOSImage
```
New-CMTaskSequence [-ApplicationName <String[]>] [-ApplyAll <Boolean>] -BootImagePackageId <String>
 [-CaptureLocallyUsingLink <Boolean>] [-CaptureNetworkSetting <Boolean>] [-CaptureUserSetting <Boolean>]
 [-CaptureWindowsSetting <Boolean>] [-ClientPackagePackageId <String>] [-ConfigureBitLocker <Boolean>]
 [-Description <String>] [-DomainAccount <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainPassword <SecureString>] [-GeneratePassword <Boolean>] [-HighPerformance <Boolean>]
 [-IgnoreInvalidApplication <Boolean>] [-InstallationLicensingMode <ServerLicensingMode>]
 [-InstallationProperty <String>] [-InstallOperatingSystemImage] -JoinDomain <JoinType>
 [-LocalAdminPassword <SecureString>] -Name <String> -OperatingSystemImageIndex <UInt32>
 -OperatingSystemImagePackageId <String> [-PartitionAndFormatTarget <Boolean>] [-ProductKey <String>]
 [-SaveLocally <Boolean>] [-SoftwareUpdateStyle <SoftwareUpdateStyleType>] [-TimeZone <TimeZoneInfo>]
 [-UserStateMigrationToolPackageId <String>] [-WorkgroupName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewInstallOSImageVhd
```
New-CMTaskSequence [-ApplicationName <String[]>] [-ApplyAll <Boolean>] -BootImagePackageId <String>
 [-ClientPackagePackageId <String>] [-ConfigureBitLocker <Boolean>] [-Description <String>]
 [-DomainAccount <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainPassword <SecureString>] [-GeneratePassword <Boolean>] [-HighPerformance <Boolean>]
 [-IgnoreInvalidApplication <Boolean>] [-InstallationLicensingMode <ServerLicensingMode>]
 [-InstallationProperty <String>] [-InstallOperatingSystemImageVhd] -JoinDomain <JoinType>
 [-LocalAdminPassword <SecureString>] -Name <String> -OperatingSystemImageIndex <UInt32>
 -OperatingSystemImagePackageId <String> [-PartitionAndFormatTarget <Boolean>] [-ProductKey <String>]
 [-TimeZone <TimeZoneInfo>] [-WorkgroupName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpgradeOSImage
```
New-CMTaskSequence [-ApplicationName <String[]>] [-HighPerformance <Boolean>]
 [-IgnoreInvalidApplication <Boolean>] -Name <String> [-ProductKey <String>]
 [-SoftwareUpdateStyle <SoftwareUpdateStyleType>] [-UpgradeOperatingSystem] -UpgradePackageId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewCustom
```
New-CMTaskSequence [-BootImagePackageId <String>] [-CustomTaskSequence] [-Description <String>]
 [-HighPerformance <Boolean>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a task sequence. You typically use a task sequence to deploy an OS to a client, but you can use them for various purposes. For more information, see [Manage task sequences to automate tasks](/mem/configmgr/osd/deploy-use/manage-task-sequences-to-automate-tasks).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a custom task sequence

This command creates a blank task sequence with the name **Custom**.

```powershell
New-CMTaskSequence -CustomTaskSequence -Name "Custom" -Description "NewCustom parameter set" -HighPerformance $false -BootImagePackageId "XYZ00002"
```

### Example 2: Create a task sequence to install an OS image

This command creates a task sequence named **Install OS image** that installs an OS image. It also includes the other parameters that apply to this scenario.

```powershell
$acct = "contoso\jqpublic"
$pwd = ConvertTo-SecureString -String "w%1H6EoxjQ&70^W" -AsPlainText -Force
$domainOU = "LDAP://OU=Workstations,OU=Devices,DC=na,DC=contoso,DC=com"

$clientProps = '/mp:mp01.contoso.com CCMDEBUGLOGGING="1" CCMLOGGINGENABLED="TRUE" CCMLOGLEVEL="0" CCMLOGMAXHISTORY="5" CCMLOGMAXSIZE="10000000" SMSCACHESIZE="15000" SMSMP=mp01.contoso.com'

$tz = Get-TimeZone -Name "Eastern Standard Time"

New-CMTaskSequence -InstallOperatingSystemImage -Name "Install OS image" -Description "NewInstallOSImage parameter set" -BootImagePackageId "XYZ00002" -HighPerformance $true -CaptureNetworkSetting $true -CaptureUserSetting $true -SaveLocally $true -CaptureLocallyUsingLink $true -UserStateMigrationToolPackageId "XYZ00001" -CaptureWindowsSetting $true -ConfigureBitLocker $true -PartitionAndFormatTarget $true -ApplyAll $false -OperatingSystemImagePackageId "XYZ001A0" -OperatingSystemImageIndex 1 -ProductKey "6NMRW-2C8FM-D24W7-TQWMY-CWH2D" -GeneratePassword $true -TimeZone $tz -JoinDomain DomainType -DomainAccount $acct -DomainName "contoso" -DomainOrganizationUnit $domainOU -DomainPassword $pwd -ClientPackagePackageId "XYZ00003" -InstallationProperty $clientProps -ApplicationName "Admin Console" -IgnoreInvalidApplication $false -SoftwareUpdateStyle All
```

### Example 3: Create a task sequence to build and capture an OS

This example creates a task sequence named **Build and capture** that builds and captures an OS image using the supplied location and account. It also includes the other parameters that apply to this scenario.

```powershell
$acct = "contoso\jqpublic"
$pwd = ConvertTo-SecureString -String "w%1H6EoxjQ&70^W" -AsPlainText -Force

$clientProps = '/mp:mp01.contoso.com CCMDEBUGLOGGING="1" CCMLOGGINGENABLED="TRUE" CCMLOGLEVEL="0" CCMLOGMAXHISTORY="5" CCMLOGMAXSIZE="10000000" SMSCACHESIZE="15000" SMSMP=mp01.contoso.com'

$tz = Get-TimeZone -Name "Eastern Standard Time"

New-CMTaskSequence -BuildOperatingSystemImage -Name "Build and capture" -Description "NewBuildOSImage parameter set" -BootImagePackageId "XYZ00002" -HighPerformance $true -ApplyAll $false -OperatingSystemImagePackageId "XYZ001A0" -OperatingSystemImageIndex 1 -ProductKey "6NMRW-2C8FM-D24W7-TQWMY-CWH2D" -GeneratePassword $true -TimeZone $tz -JoinDomain WorkgroupType -WorkgroupName "groupwork" -ClientPackagePackageId "XYZ00003" -InstallationProperty $clientProps -ApplicationName "Admin Console" -IgnoreInvalidApplication $true -SoftwareUpdateStyle All -OperatingSystemFilePath "\\server1\images\capture.wim" -ImageDescription "image description" -ImageVersion "image version 1" -CreatedBy "jqpublic" -OperatingSystemFileAccount $acct -OperatingSystemFileAccountPassword $pwd 
```

### Example 4: Create a task sequence to upgrade an OS

This command creates the task sequence named **In-place upgrade** and specifies that it will upgrade the OS using the upgrade package with the ID **XYZ02EBA**.

```powershell
New-CMTaskSequence -UpgradeOperatingSystem -Name "In-place upgrade" -UpgradePackageId "XYZ02EBA" -SoftwareUpdateStyle All
```

## PARAMETERS

### -ApplicationName

Specify an array of application names to install during the task sequence. This parameter configures the [Install Application](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallApplication) task sequence step.

```yaml
Type: String[]
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyAll

In the build and capture scenario, the state of this parameter determines the following behaviors:

- `$true`: The task sequence doesn't format & partition the disk before it applies the OS image.

- `$false`: The task sequence includes the [Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk) steps before it applies the OS image.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases: ApplyAllImages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImagePackageId

Specify the ID of a boot image package to use with a task sequence that deploys an OS. This value is a standard package ID, for example `XYZ00005`.

This parameter configures the task sequence properties.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewCustom
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BuildOperatingSystemImage

Add this parameter to create a task sequence for the build and capture scenario. For more information, see [Create a task sequence to capture an OS](/mem/configmgr/osd/deploy-use/create-a-task-sequence-to-capture-an-operating-system).

```yaml
Type: SwitchParameter
Parameter Sets: NewBuildOSImage
Aliases: BuildOperatingSystemImageOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureLocallyUsingLink

When you enable the **SaveLocally** parameter to save user settings and files locally, set this parameter to **$true** to capture locally by using links instead of by copying files. The links that Configuration Manager uses to store the user state locally are referred to as hard-links.

The cmdlet ignores this parameter if **SaveLocally** is **$false**.

This parameter configures the [Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState) step.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases: CaptureLocallyUsingLinks

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureNetworkSetting

Set this parameter to **$true** to enable the task sequence to capture network settings. When you enable this option, the task sequence includes the [Capture Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureNetworkSettings) step.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureUserSetting

Set this parameter to **$true** to enable the task sequence to capture user settings and files. When you enable this option, the task sequence includes the [Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState) step. Also use the **UserStateMigrationToolPackageId** parameter.

Use **SaveLocally** and **CaptureLocallyUsingLink** to configure where the task sequence saves the user state.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureWindowsSetting

Set this parameter to **$true** to enable the task sequence to capture Windows settings. When you enable this option, the task sequence includes the [Capture Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureWindowsSettings) step.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientPackagePackageId

Specify the ID of the client package to install when the task sequence runs. This value is a standard package ID, for example, `XYZ00003`. Site assignment and client configuration happen automatically. You can specify extra installation parameters with the **InstallationProperty** parameter.

This parameter configures the [Setup Windows and ConfigMgr](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetupWindowsandConfigMgr) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureBitLocker

Set this parameter to **$true** to configure the task sequence for use with BitLocker. When you enable this option, the task sequence includes the following steps:

- [Disable BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_DisableBitLocker)
- [Pre-provision BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PreProvisionBitLocker)
- [Enable BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_EnableBitLocker)

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreatedBy

For the build and capture scenario, specify an optional string that's on the captured image file for who created it. The maximum length is 255 characters.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomTaskSequence

Add this parameter to create a custom task sequence that contains no steps. For more information, see [Create a custom task sequence](/mem/configmgr/osd/deploy-use/create-a-custom-task-sequence).

You can then use the 35 **New-CMTSStep** cmdlets to add steps to the custom task sequence. For more information, see [About task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps). Each section describes the task sequence steps, with links to the associated cmdlets.

```yaml
Type: SwitchParameter
Parameter Sets: NewCustom
Aliases: CustomOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description for the task sequence. The maximum length is 512 characters. This parameter configures the task sequence properties.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, NewCustom
Aliases: TaskSequenceDescription

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

### -DomainAccount

Specify an account that has the necessary permissions to join the computer to the domain. Use the following format: `Domain\User`. For more information, see [ask sequence domain join account](/mem/configmgr/core/plan-design/hierarchy/accounts#task-sequence-domain-join-account).

Use the **DomainName** parameter to specify the domain name, and **DomainPassword** to specify this account's password.

This parameter configures the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName

Specify the name of a domain to have the computer join when it runs the task sequence. This parameter configures the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step.

Use the **DomainAccount** parameter to specify an account that has permissions to join this domain. You can also use the **DomainOrganizationUnit** parameter to specify an OU in which to create the computer account.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainOrganizationUnit

Specify a domain organizational unit (OU) in which to create the computer account in the domain. The format of this value is the Lightweight Directory Access Protocol (LDAP) path, for example: `LDAP//OU=OSD staging,DC=contoso,DC=com`. Specify an OU in the domain that you specified in the **DomainName** parameter.

If an existing computer account is already in an OU, Active Directory doesn't allow you to change the OU and it ignores this setting.

This parameter configures the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword

Specify a secure string for the password of the account that you specified with the **DomainAccount** parameter.

This parameter configures the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
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

### -GeneratePassword

Set this parameter to **$true** to randomly generate the local administrator password and disable the account. This configuration is recommended.

This parameter configures the [Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings) task sequence step.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighPerformance

Set this parameter to **$true** to enable the task sequence option to run as high-performance power plan. This parameter configures the task sequence properties. For more information, see [Performance improvements for power plans](/mem/configmgr/osd/deploy-use/manage-task-sequences-to-automate-tasks#bkmk_perf).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreInvalidApplication

If you set this parameter to **$true**, the task sequence continues installing applications in the list if an application installation fails. Use this parameter with the **ApplicationName** parameter.

This parameter configures the [Install Application](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallApplication) task sequence step.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageDescription

For the build and capture scenario, specify an optional string that describes the captured image file. The maximum length is 255 characters.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageVersion

For the build and capture scenario, specify an optional string as the version of the captured image file. You define this value, it doesn't have to be the OS version. The maximum length is 32 characters.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationLicensingMode

This setting only applies to legacy versions of Windows that are no longer supported. Starting in version 2010, the setting is no longer visible in the task sequence editor. Existing task sequences that still use this setting will continue to function the same.

```yaml
Type: ServerLicensingMode
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:
Accepted values: NonSpecify, PerSeat, PerServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProperty

Specify any extra installation properties to use when the task sequence installs the Configuration Manager client. Site assignment and the default configuration are automatically specified by the task sequence. To enter multiple installation properties, separate them with a space. If a property contains spaces, surround it by quotation marks (`"`). For more information, see [About client installation parameters and properties in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-installation-properties).

This list can't include **SMSSITECODE**.

This parameter configures the [Setup Windows and ConfigMgr](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetupWindowsandConfigMgr) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallOperatingSystemImage

Add this parameter to create a task sequence for the install OS image scenario. For more information, see [Create a task sequence to install an OS](/mem/configmgr/osd/deploy-use/create-a-task-sequence-to-install-an-operating-system).

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallOSImage
Aliases: InstallOperatingSystemImageOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallOperatingSystemImageVhd

Don't use this parameter. Support for VHD files was removed in Configuration Manager version 1710.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallOSImageVhd
Aliases: InstallOperatingSystemImageVhdOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain

Use this parameter to configure the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step. The computer needs to either join a workgroup or a domain.

- `DomainType`: Join a domain. Also specify **DomainName**, **DomainAccount**, and **DomainPassword**. You can also use **DomainOrganizationUnit**.

- `WorkgroupType`: Join a workgroup. Also specify **WorkgroupName**. Use this value with the **BuildOperatingSystemImage** parameter. In the build and capture scenario, the task sequence always joins a workgroup before it captures the image.

```yaml
Type: JoinType
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:
Accepted values: DomainType, WorkgroupType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalAdminPassword

If you don't use the recommended option to **GeneratePassword**, use this parameter to specify a secure string as the local Administrator password.

This parameter configures the [Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings) task sequence step.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumServerConnection

This setting only applies to legacy versions of Windows that are no longer supported. Starting in version 2010, the setting is no longer visible in the task sequence editor. Existing task sequences that still use this setting will continue to function the same.

```yaml
Type: Int32
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for the task sequence. The maximum length is 50 characters. This parameter configures the task sequence properties.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskSequenceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFileAccount

For the build and capture scenario, specify the name of a domain account that has permissions to the network share that you specify in the **OperatingSystemFilePath** parameter. Use **OperatingSystemFileAccountPassword** to set the account password.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases: CaptureOperatingSystemFileAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFileAccountPassword

For the build and capture scenario, specify a secure string for the password of the **OperatingSystemFileAccount**.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFilePath

For the build and capture scenario, specify the file path to the network location that Configuration Manager uses to store the captured OS image. The path includes the file name with a `.wim` file extension. Use **OperatingSystemFileAccount** and **OperatingSystemFileAccountPassword** to specify an account that has access to this location.

This parameter configures the [Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases: CaptureOperatingSystemFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageIndex

Specify the index of the OS image to install for the [Apply OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage) task sequence step.

```yaml
Type: UInt32
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImagePackageId

Specify the ID of the OS image package to install. Use **OperatingSystemImageIndex** to specify the image index. This value is a standard package ID, for example `XYZ00050`.

This parameter configures the [Apply OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionAndFormatTarget

Set this parameter to **$true** for the task sequence to partition and format the target computer before it installs the OS.

This parameter configures the [Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk) task sequence step.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductKey

Specify the Windows product key for the OS installation.

This parameter configures the [Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases: InstallationProductKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SaveLocally

If you enable the **CaptureUserSetting** parameter, then use this parameter to determine where the task sequence saves the captured user state:

- `$true`: The task sequence configures the local state location, and captures locally by using links instead of by copying files. This value configures the [Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState) step.

  - Use the **CaptureLocallyUsingLink** parameter to configure the use of hard-links.

- `$false`: The task sequence includes steps to use a state migration point. It configures the following steps:

  - [Request State Store](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RequestStateStore)
  - [Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState)
  - [Release State Store](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ReleaseStateStore)

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateStyle

Specify whether to install software updates during the task sequence. The values determine the type of software update deployment:

- `All`: Available for installation, all software updates
- `Mandatory`: Required for installation, mandatory software updates only
- `NoInstall`: Don't install any software updates

This parameter configures the [Install Software Updates](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallSoftwareUpdates) task sequence step.

```yaml
Type: SoftwareUpdateStyleType
Parameter Sets: NewBuildOSImage, NewInstallOSImage, UpgradeOSImage
Aliases:
Accepted values: All, Mandatory, NoInstall

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone

Specify the default time zone for this installation of Windows. To get a time zone object, use the built-in [Get-TimeZone](/powershell/module/microsoft.powershell.management/get-timezone) cmdlet.

This parameter configures the [Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings) task sequence step.

```yaml
Type: TimeZoneInfo
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeOperatingSystem

Add this parameter to create a task sequence for the OS upgrade scenario. For more information, see [Create a task sequence to upgrade an OS](/mem/configmgr/osd/deploy-use/create-a-task-sequence-to-upgrade-an-operating-system).

```yaml
Type: SwitchParameter
Parameter Sets: UpgradeOSImage
Aliases: UpgradeOperatingSystemOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePackageId

Specify the ID of the OS upgrade package to use. This value is a standard package ID, for example `XYZ00052`.

This parameter configures the [Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage) task sequence step.

```yaml
Type: String
Parameter Sets: UpgradeOSImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserStateMigrationToolPackageId

When you set **CaptureUserSetting** to **$true**, use this parameter to specify the ID of the User State Migration Tool (USMT) package. This value is a standard package ID, for example `XYZ00012`.

This parameter configures the [Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState) and [Restore User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RestoreUserState) steps.

```yaml
Type: String
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkgroupName

If you set the **JoinDomain** parameter to `WorkgroupType`, use this parameter to specify the workgroup name. This parameter configures the [Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings) task sequence step.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequencePackage

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequencePackage server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequencepackage-server-wmi-class).

On the [Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings) task sequence step, this cmdlet sets the **User name** value to the user that runs the cmdlet, and the **Organization name** to the computer name where the cmdlet runs.

You can't configure all task sequence and step settings with this cmdlet. To configure other settings, use [Set-CMTaskSequence](Set-CMTaskSequence.md) and the **Set-CMTSStep** cmdlets, for example, [Set-CMTSStepApplyOperatingSystem](Set-CMTSStepApplyOperatingSystem.md).

## RELATED LINKS

[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
[New-CMTaskSequenceMedia](New-CMTaskSequenceMedia.md)

[New-CMTaskSequenceDeployment](New-CMTaskSequenceDeployment.md)

[About task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps)
