---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/03/2021
online version:
schema: 2.0.0
---

# Get-CMSoftwareUpdateContentInfo

## SYNOPSIS

Get software update content information.

## SYNTAX

### SearchById (Default)
```
Get-CMSoftwareUpdateContentInfo -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMSoftwareUpdateContentInfo -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByName
```
Get-CMSoftwareUpdateContentInfo -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUniqueId
```
Get-CMSoftwareUpdateContentInfo -UniqueId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get software update content information. For example,

- File name
- File size
- SHA-1 hash
- Source URL

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get software update content information for a specific update

This example first gets the software updates whose article ID is **5004237**. The second line then passes the array of updates as the input object, and gets the content information for the first array member.

```powershell
$update = Get-CMSoftwareUpdate -ArticleId "5004237" -Fast
Get-CMSoftwareUpdateContentInfo -InputObject $update[1]
```

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

Specify the **CI_ID** of the software update to get its content information. This value is an integer, for example `1584792`.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a software update object to get its content information. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

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

### -Name

Specify the localized display name of a software update to get its content information. It matches the exact string, it doesn't accept wildcard characters.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniqueId

Specify the **Unique Update ID** of the software update to get its content information. This value is a GUID, and also the **CI_UniqueID** property on the software update object.

```yaml
Type: String
Parameter Sets: SearchByUniqueId
Aliases: CI_UniqueID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_CIContentFiles

### IResultObject#SMS_CIContentFiles

## NOTES

For more information on this return object and its properties, see [SMS_CIContentFiles server WMI class](/mem/configmgr/develop/reference/sum/sms_cicontentfiles-server-wmi-class).

## RELATED LINKS

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)
