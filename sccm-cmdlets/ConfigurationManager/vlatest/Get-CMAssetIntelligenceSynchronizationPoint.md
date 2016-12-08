---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834120
schema: 2.0.0
ms.assetid: 19923FBC-EDF0-4BB5-8FEE-F0B4428D2413
---

# Get-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Gets Asset Intelligence synchronization points.

## SYNTAX

### SearchByName
```
Get-CMAssetIntelligenceSynchronizationPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMAssetIntelligenceSynchronizationPoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAssetIntelligenceSynchronizationPoint** cmdlet gets one or more Asset Intelligence synchronization points.
Microsoft System Center Configuration Manager uses the Asset Intelligence synchronization point site system role to connect System Center Configuration Manager sites to System Center Online to synchronize Asset Intelligence catalog information.

## EXAMPLES

### Example 1: Get an Asset Intelligence synchronization point
```
PS C:\>Get-CMAssetIntelligenceSynchronizationPoint
```

This command gets an Asset Intelligence synchronization point.

## PARAMETERS

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

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

### -SiteCode


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

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](./Add-CMAssetIntelligenceSynchronizationPoint.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](./Remove-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](./Set-CMAssetIntelligenceSynchronizationPoint.md)


