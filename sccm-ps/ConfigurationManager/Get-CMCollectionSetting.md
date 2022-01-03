---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMCollectionSetting
---

# Get-CMCollectionSetting

## SYNOPSIS

Get the settings for a collection.

## SYNTAX

### ByValue (Default)
```
Get-CMCollectionSetting [-CollectionType <CollectionType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionSetting -CollectionId <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMCollectionSetting -CollectionName <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the settings for a collection. These settings include properties for device variables, power management, and maintenance windows. In most instances, use the dedicated cmdlets for these properties, for example:

- [Get-CMDeviceCollectionVariable](Get-CMDeviceCollectionVariable.md)
- [Set-CMCollectionPowerManagement](Set-CMCollectionPowerManagement.md)
- [Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the settings for a collection by using the pipeline

This command gets the collection object with the ID of **XYZ00014** and uses the pipeline operator to pass the object to **Get-CMCollectionSetting**, which gets the device collection settings for the collection object.

```powershell
Get-CMCollection -Id XYZ00014 | Get-CMCollectionSetting -CollectionType Device
```

### Example 2: Get the settings for a collection by name

This command gets the collection settings for the device collection named **Devicecol1**.

```powershell
Get-CMCollectionSetting -CollectionName "Devicecol1"
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to get its settings. This value is the **CollectionID** property, for example, `XYZ00012`.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of the collection to get its settings.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionType

Filter the type of collection to get.

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

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

### -InputObject

Specify a collection object to get its settings. To get this object, use one of the following cmdlets:

- [Get-CMCollection](Get-CMCollection.md)
- [Get-CMDeviceCollection](Get-CMDeviceCollection.md)
- [Get-CMUserCollection](Get-CMUserCollection.md)

You can also use the pipeline operator (`|`) to pass a collection object to **Get-CMCollectionMemeber** on the command line.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

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

### System.Object

## NOTES

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections)
