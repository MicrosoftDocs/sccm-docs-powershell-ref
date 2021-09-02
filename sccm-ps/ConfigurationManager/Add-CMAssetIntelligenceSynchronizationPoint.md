---
description: Installs an Asset Intelligence synchronization point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/27/2019
schema: 2.0.0
title: Add-CMAssetIntelligenceSynchronizationPoint
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
Configuration Manager uses the Asset Intelligence synchronization point site system role to connect Configuration Manager sites to System Center Online to synchronize Asset Intelligence catalog information.

You can install the Asset Intelligence synchronization point only on a site system located at the top-level site of the Configuration Manager hierarchy.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Install an Asset Intelligence synchronization point
```
PS XYZ:\>Add-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-TSQA04.CORP.CONTOSO.COM"
```

This command installs an Asset Intelligence synchronization point on the site system server named CMDIV-TSQA04.CORP.CONTOSO.COM.

### Example 2: Install a scheduled Asset Intelligence synchronization point
```
PS XYZ:\> $Sc = New-CMSchedule -DayOfWeek Friday -RecurCount 2
PS XYZ:\> Add-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-TSQA04.CORP.CONTOSO.COM" -CertificateFile "\\Contoso01\CM\ACDataFile\AIpfx.pfx" -ScheduleToken $Sc
```

This first command creates a Configuration Manager schedule token that specifies an event that occurs once a week for three weeks on Fridays.
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

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)

[New-CMSchedule](New-CMSchedule.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](Remove-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)
