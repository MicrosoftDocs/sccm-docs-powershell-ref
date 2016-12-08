---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833659
schema: 2.0.0
ms.assetid: A6085846-7C0C-49CE-B542-65E240999450
---

# Set-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Enables or disables an Asset Intelligence synchronization point.

## SYNTAX

```
Set-CMAssetIntelligenceSynchronizationPoint [-Enable <Boolean>] [-CertificateFile <String>]
 [-EnableSynchronization <Boolean>] [-Schedule <IResultObject>] [-InputObject <IResultObject>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAssetIntelligenceSynchronizationPoint** cmdlet enables or disables one or more Asset Intelligence synchronization points.
You must enable the Asset Intelligence synchronization point to perform scheduled Asset Intelligence catalog synchronizations with System Center Online.

## EXAMPLES

### Example 1: Enable an Asset Intelligence synchronization point
```
PS C:\> Set-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM" -Enabled $True
```

This command enables the Asset Intelligence synchronization point on the site server named CMDIV-WEST04.CORP.CONTOSO.COM.

## PARAMETERS

### -CertificateFile


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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enable


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

### -EnableSynchronization


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
Specifies an Asset Intelligence synchronization point object.
To obtain a CMAssetIntelligenceSynchronizationPoint object, use the Get-CMAssetIntelligenceSynchronizationPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: AssetIntelligenceUpdateServicePoint
Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](./New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: ScheduleToken
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](./Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](./Get-CMAssetIntelligenceSynchronizationPoint.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](./Remove-CMAssetIntelligenceSynchronizationPoint.md)
