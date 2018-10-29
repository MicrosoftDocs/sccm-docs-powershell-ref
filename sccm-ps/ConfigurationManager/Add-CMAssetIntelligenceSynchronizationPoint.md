---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: B2B9CF97-719D-4F30-87C9-9ED6F3A5A798
online version: https://go.microsoft.com/fwlink/?linkid=833598
schema: 2.0.0
---

# Add-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Installs an Asset Intelligence synchronization point.

## SYNTAX

### AISyncPointByValue (Default)
```
Add-CMAssetIntelligenceSynchronizationPoint [-CertificateFile <String>] -InputObject <IResultObject>
 [-Schedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AISyncPoint
```
Add-CMAssetIntelligenceSynchronizationPoint [-CertificateFile <String>] [-Schedule <IResultObject>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMAssetIntelligenceSynchronizationPoint** cmdlet installs an Asset Intelligence synchronization point.
Microsoft System Center Configuration Manager uses the Asset Intelligence synchronization point site system role to connect System Center Configuration Manager sites to System Center Online to synchronize Asset Intelligence catalog information.

You can install the Asset Intelligence synchronization point only on a site system located at the top-level site of the System Center Configuration Manager hierarchy.

## EXAMPLES

### Example 1: Install an Asset Intelligence synchronization point
```
PS C:\>Add-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-TSQA04.CORP.CONTOSO.COM"
```

This command installs an Asset Intelligence synchronization point on the site system server named CMDIV-TSQA04.CORP.CONTOSO.COM.

### Example 2: Install a scheduled Asset Intelligence synchronization point
```
PS C:\> $Sc = New-CMSchedule -DayOfWeek Friday -RecurCount 2
PS C:\> Add-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-TSQA04.CORP.CONTOSO.COM" -CertificateFile "\\Contoso01\CM\ACDataFile\AIpfx.pfx" -ScheduleToken $Sc
```

This first command creates a System Center Configuration Manager schedule token that specifies an event that occurs once a week for three weeks on Fridays.
The command stores the results in the $Sc variable.

The second command installs an Asset Intelligence synchronization point on the site system server named CMDIV-TSQA04.CORP.CONTOSO.COM, specifying the schedule stored in $Sc.
The command also specifies the System Center Online authentication certificate (.pfx) file.

## PARAMETERS

### -CertificateFile
Specifies the path to a System Center Online authentication certificate (.pfx) file.

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
Parameter Sets: AISyncPointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -SiteSystemServerName
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system role.

```yaml
Type: String
Parameter Sets: AISyncPoint
Aliases: Name, ServerName

Required: True
Position: 0
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

[Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)

[New-CMSchedule](New-CMSchedule.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](Remove-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)
