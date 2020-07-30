---
description: Gets a Configuration Manager device.
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDevice
---

# Get-CMDevice

## SYNOPSIS
Gets a Configuration Manager device.

## SYNTAX

### ByName (Default)
```
Get-CMDevice [-Name <String>] [-Fast] [-CollectionMember] [-Resource] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMDevice -CollectionName <String> [-Name <String>] [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDevice -CollectionId <String> [-Name <String>] [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -ThreatId <String> [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -ThreatName <String> [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -InputObject <IResultObject> [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMDevice -Collection <IResultObject> [-Name <String>] [-Fast] [-CollectionMember] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMDevice -ResourceId <Int32> [-Fast] [-CollectionMember] [-Resource] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDevice** cmdlet gets a Microsoft System Center Configuration Manager device.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a device by collection ID
```
PS XYZ:\> Get-CMDevice -CollectionID "SMSDM003"
```

This command gets all the device objects in the device collection with the ID of SMSDM003.

### Example 2: Get a device by name
```
PS XYZ:\> Get-CMDevice -CollectionName "All systems" -Name "Win10-86-33"
```

This command gets the device named Win10-86-33 in the device collection named All systems.

## PARAMETERS

### -Collection
Specifies a device collection object. To obtain a device collection object, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies an ID for a device collection.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients, SearchByNameMandatoryForViewInfectedClients, SearchByValueMandatoryForViewInfectedClients
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionMember
{{ Fill CollectionMember Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CollectionMemberInstance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a device collection.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance. If lazy properties are not used, this parameter should be specified.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
Specifies an object that represents a threat.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatoryForViewInfectedClients
Aliases: Threat

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device.

```yaml
Type: String
Parameter Sets: ByName, SearchByNameMandatory, SearchByIdMandatory, SearchByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resource
{{ Fill Resource Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ResourceInstance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the resource ID of a device.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: Id, DeviceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatId
Specifies an ID of a threat.

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients
Aliases: ThreatNameId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatName
Specifies a name of a threat.

```yaml
Type: String
Parameter Sets: SearchByNameMandatoryForViewInfectedClients
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_CombinedDeviceResources

### IResultObject#SMS_CombinedDeviceResources

## NOTES

## RELATED LINKS

[Approve-CMDevice](Approve-CMDevice.md)

[Block-CMDevice](Block-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Remove-CMDevice](Remove-CMDevice.md)

[Unblock-CMDevice](Unblock-CMDevice.md)
