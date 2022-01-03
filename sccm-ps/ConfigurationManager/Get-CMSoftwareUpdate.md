---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Get-CMSoftwareUpdate
---

# Get-CMSoftwareUpdate

## SYNOPSIS

Get a software update.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdate [-ArticleId <String>] [-BulletinId <String>] [-Category <IResultObject[]>]
 [-CategoryName <String[]>] [-DatePostedMax <DateTime>] [-DatePostedMin <DateTime>]
 [-DateRevisedMax <DateTime>] [-DateRevisedMin <DateTime>] [-EulaExist <Boolean>] [-Fast] [-IncludeUpgrade]
 [-IsContentProvisioned <Boolean>] [-IsDeployed <Boolean>] [-IsExpired <Boolean>] [-IsLatest <Boolean>]
 [-IsOfflineServiceable <Boolean>] [-IsSuperseded <Boolean>] [-IsUserDefined <Boolean>] [-Name <String>]
 [-OnlyExpired] [-Severity <CustomSeverityType>] [-Vendor <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdate [-Fast] -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroup
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroupIdMandatory
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroupId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroupNameMandatory
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroupName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more software updates.

For more information, see [Software update management documentation](/mem/configmgr/sum/) in the core docs.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get downloaded software updates

This command gets all software updates that the site has downloaded.

```powershell
Get-CMSoftwareUpdate -IsContentProvisioned $True
```

### Example 2: Get software updates by update group

This command first gets the software update group object named **TestSUgroup10**. It then uses the pipeline operator to pass the object to **Get-CMSoftwareUpdate**. The result is the list of all software updates for the software update group.

```powershell
Get-CMSoftwareUpdateGroup -Name "TestSUgroup10" | Get-CMSoftwareUpdate
```

## PARAMETERS

### -ArticleId

Specify the **Article ID** of a software update. For example, `4571687`.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -BulletinId

Specify the **Bulletin ID** of a software update. For example, `MS18-952`.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Category

Specify the category of a software update. To get a category object, use the [Get-CMSoftwareUpdateCategory](Get-CMSoftwareUpdateCategory.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CategoryName

Specify an array of category names for software updates.

```yaml
Type: String[]
Parameter Sets: SearchByName
Aliases: CategoryNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatePostedMax

Specify the latest date that a software update was released.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatePostedMin

Specify the earliest date that a software update was released.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateRevisedMax

Specify the latest date that a software update was revised.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateRevisedMin

Specify the earliest date that a software update was revised.

```yaml
Type: DateTime
Parameter Sets: SearchByName
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

### -EulaExist

Set this parameter to `$true` to filter results for all updates that have a license agreement.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases: EulaExists

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -Id

Specifies the ID of a software update. This value is the **CI_ID**, for example `143404`.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeUpgrade

Add this parameter to include software updates in the upgrade category.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByName
Aliases: IncludeUpgrades

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsContentProvisioned

Set this parameter to `$true` to filter results for all updates for which the site has downloaded content.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDeployed

Set this parameter to `$true` to filter results for all updates that are deployed.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsExpired

Set this parameter to `$true` to filter results for all updates that are expired.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsLatest

Set this parameter to `$true` to filter results for the latest version of the software update.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsOfflineServiceable

Set this parameter to `$true` to filter results for all updates that are offline-serviceable. You can use the DISM command-line tool to inject these updates into an OS image.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSuperseded

Set this parameter to `$true` to filter results for all updates that are superseded.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsUserDefined

Set this parameter to `$true` to filter results for all updates that are user-defined.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of a software update. This parameter compares against the localized display name attribute.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -OnlyExpired

Add this parameter to only search for expired software updates.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Severity

Specify the severity of the software update.

```yaml
Type: CustomSeverityType
Parameter Sets: SearchByName
Aliases:
Accepted values: None, Low, Moderate, Important, Critical

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateGroup

Specify software update group object. To get this object, use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByUpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UpdateGroupId

Specify an array of IDs of software update groups. This value is the **CI_ID** or **Config Item ID** of the software update group. For example, `107078`.

```yaml
Type: String[]
Parameter Sets: SearchByUpdateGroupIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateGroupName

Specify an array of names of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByUpdateGroupNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vendor

Applies to version 2010 and later. Specify the name of the software update vendor. The vendor for most software updates is `"Microsoft"`. If you configure third-party software updates, use this value to filter on other update vendors.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_SoftwareUpdate

### IResultObject#SMS_SoftwareUpdate

## NOTES

For more information on this return object and its properties, see [SMS_SoftwareUpdate server WMI class](/mem/configmgr/develop/reference/sum/sms_softwareupdate-server-wmi-class).

## RELATED LINKS

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)

[Set-CMSoftwareUpdate](Set-CMSoftwareUpdate.md)

[Sync-CMSoftwareUpdate](Sync-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateCategory](Get-CMSoftwareUpdateCategory.md)

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Get-CMSoftwareUpdateContentInfo](Get-CMSoftwareUpdateContentInfo.md)
