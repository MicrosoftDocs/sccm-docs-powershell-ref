---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
schema: 2.0.0
title: Get-CMDistributionStatus
---

# Get-CMDistributionStatus

## SYNOPSIS

Get the content status of an object.

## SYNTAX

### SearchById (Default)
```
Get-CMDistributionStatus [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMDistributionStatus -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the content status of an object. For example, a package, an application, or a boot image. The results of this command are the same as what displays in the Configuration Manager console in the **Content Status** area of the **Summary** tab of the details pane. For more information, see [Monitor content you distribute with Configuration Manager](/mem/configmgr/core/servers/deploy/configure/monitor-content-you-have-distributed#content-status-monitoring).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get status for an application using its package ID

The first command gets the package ID of an application named **WebView2 Redist (x86)** and stores it in the variable **PackageId**. The second command uses the package ID as a parameter to **Get-CMDistributionStatus**, which gets the distribution status of the application.

```powershell
$PackageId = (Get-CMApplication -Name 'WebView2 Redist (x86)').PackageID
Get-CMDistributionStatus -Id $PackageId
```

```output
SmsProviderObjectPath : SMS_ObjectContentExtraInfo.ObjectID="ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/Application_8
                        8fe14d8-73b2-43bc-897e-08232861c864"
DateCreated           : 11/5/2020 12:59:19
Description           : Installs the WebView2 cab redist to the console.
FeatureType           : 8
LastUpdateDate        : 2/24/2021 00:02:47
NumberErrors          : 0
NumberInProgress      : 0
NumberSuccess         : 3
NumberUnknown         : 0
ObjectID              : ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/Application_88fe14d8-73b2-43bc-897e-08232861c864
ObjectType            : 512
ObjectTypeID          : 31
PackageID             : XYZ00810
SoftwareName          : WebView2 Redist (x86)
SourceSite            : XYZ
SourceSize            : 123389
SourceVersion         : 1
Targeted              : 3
```

You can see from this output that the application was distributed to three distribution points, because the **Targeted** property is `3`. You can also see that the site successfully distributed the content, because the **NumberSuccess** property is also `3`. For more information about these properties, see [SMS_ObjectContentExtraInfo server WMI class](/mem/configmgr/develop/reference/core/servers/console/sms_objectcontentextrainfo-server-wmi-class).

## PARAMETERS

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

Specify the package ID for the object to get its content status. This value is a standard package ID, for example, `XYZ0005E2`.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: PackageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object to get its content status. To get this object, use one of the following cmdlets:

- [Get-CMApplication](Get-CMApplication.md)
- [Get-CMBootImage](Get-CMBootImage.md)
- [Get-CMDriverPackage](Get-CMDriverPackage.md)
- [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) (OS upgrade package)
- [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)
- [Get-CMPackage](Get-CMPackage.md)
- [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)
- [Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_ObjectContentExtraInfo, IResultObject#SMS_ObjectContentExtraInfo
## NOTES

For more information on this return object and its properties, see [SMS_ObjectContentExtraInfo server WMI class](/mem/configmgr/develop/reference/core/servers/console/sms_objectcontentextrainfo-server-wmi-class).

## RELATED LINKS

[Monitor content you distribute with Configuration Manager](/mem/configmgr/core/servers/deploy/configure/monitor-content-you-have-distributed#content-status-monitoring)
