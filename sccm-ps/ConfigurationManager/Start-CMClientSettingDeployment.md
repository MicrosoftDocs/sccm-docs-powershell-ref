---
description: Deploys client settings to devices in a collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Start-CMClientSettingDeployment
---

# Start-CMClientSettingDeployment

## SYNOPSIS
(Deprecated) Deploys client settings to devices in a collection.

## SYNTAX

### SearchByClientSettingName_CollectionValue (Default)
```
Start-CMClientSettingDeployment -ClientSettingName <String> -Collection <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingValue_CollectionId
```
Start-CMClientSettingDeployment -ClientSetting <IResultObject> -CollectionId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingValue_CollectionName
```
Start-CMClientSettingDeployment -ClientSetting <IResultObject> -CollectionName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingValue_CollectionValue
```
Start-CMClientSettingDeployment -ClientSetting <IResultObject> -Collection <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingId_CollectionId
```
Start-CMClientSettingDeployment -ClientSettingId <String> -CollectionId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingId_CollectionName
```
Start-CMClientSettingDeployment -ClientSettingId <String> -CollectionName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingId_CollectionValue
```
Start-CMClientSettingDeployment -ClientSettingId <String> -Collection <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingName_CollectionId
```
Start-CMClientSettingDeployment -ClientSettingName <String> -CollectionId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByClientSettingName_CollectionName
```
Start-CMClientSettingDeployment -ClientSettingName <String> -CollectionName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMClientSettingDeployment** cmdlet deploys client settings to devices in a Configuration Manager collection.
Specify the client setting object by using its name or ID, or you can use the **Get-CMClientSetting** cmdlet to get a client setting object.
Specify the collection to apply the settings to by using its name or ID, or you can use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet to get a device collection.

For more information about client settings, see [About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!IMPORTANT]
> Starting in version 2107, this cmdlet is deprecated and may be removed in a future release. Instead use the [New-CMClientSettingDeployment](New-CMClientSettingDeployment.md) cmdlet.

## EXAMPLES

### Example 1: Deploy a client setting object by using its ID to a named collection
```
PS XYZ:\> Start-CMClientSettingDeployment -ClientSettingId "CSI1023" -CollectionName "General Computer Collection"
```

This command starts deployment of the client setting object that has the ID CSI1023 for the collection named General Computer Collection.

### Example 2: Deploy a client setting object by using a variable
```
PS XYZ:\> $CSID = Get-CMClientSetting -Id "CSI1023"
PS XYZ:\> Start-CMClientSettingDeployment -ClientSetting $CSID -CollectionName "General Computer Collection"
```

The first command gets a client setting object that has the ID CSI1023, and saves it in the $CSID variable.

The second command starts deployment of the client setting object in the $CSID variable to the collection named General Computer Collection.

## PARAMETERS

### -ClientSetting
Specifies a client setting object.
To obtain a client setting object, use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByClientSettingValue_CollectionId, SearchByClientSettingValue_CollectionName, SearchByClientSettingValue_CollectionValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ClientSettingId
Specifies the ID of a client setting object.

```yaml
Type: String
Parameter Sets: SearchByClientSettingId_CollectionId, SearchByClientSettingId_CollectionName, SearchByClientSettingId_CollectionValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientSettingName
Specifies the name of a client setting object.

```yaml
Type: String
Parameter Sets: SearchByClientSettingName_CollectionValue, SearchByClientSettingName_CollectionId, SearchByClientSettingName_CollectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection
Specifies a Configuration Manager collection object.
To obtain a collection object, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet.
Configuration Manager applies the client settings to the members of this collection.

```yaml
Type: IResultObject
Parameter Sets: SearchByClientSettingName_CollectionValue, SearchByClientSettingValue_CollectionValue, SearchByClientSettingId_CollectionValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of a Configuration Manager collection.
Configuration Manager applies the client settings to the members of this collection.

```yaml
Type: String
Parameter Sets: SearchByClientSettingValue_CollectionId, SearchByClientSettingId_CollectionId, SearchByClientSettingName_CollectionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a Configuration Manager collection.
Configuration Manager applies the client settings to the members of this collection.

```yaml
Type: String
Parameter Sets: SearchByClientSettingValue_CollectionName, SearchByClientSettingId_CollectionName, SearchByClientSettingName_CollectionName
Aliases:

Required: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMClientSetting](Get-CMClientSetting.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
