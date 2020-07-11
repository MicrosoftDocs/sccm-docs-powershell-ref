---
description: Changes database settings for a Configuration Manager database.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMDatabaseProperty
---

# Set-CMDatabaseProperty

## SYNOPSIS
Changes database settings for a Configuration Manager database.

## SYNTAX

```
Set-CMDatabaseProperty [-SiteCode <String>] [-EnableDataCompression <Boolean>]
 [-SqlServerServiceBrokerPort <Int32>] [-DataRetentionDays <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDatabaseProperty** cmdlet changes database settings for a Microsoft System Center Configuration Manager site database.
Specify the Configuration Manager site code for the database that you want to modify.

You can modify whether the database uses data compression, the Service Broker port for the computer that runs Microsoft SQL Server, and the length of time that the database keeps data.
You can use the [Get-CMDatabaseProperty](Get-CMDatabaseProperty.md) cmdlet to see current values for these properties.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change settings for a database
```
PS XYZ:\> Set-CMDatabaseProperty -SiteCode "CM2" -DataRetentionPeriodDays 10 -EnableDataCompression $False -SqlServerServiceBrokerPort 80
```

This command makes changes to the database for the site that has the site code CM2.
The command sets the data retention period to 10 days, disables data compression, and specifies a port for the SQL Server Service Broker.

## PARAMETERS

### -DataRetentionDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DataRetentionPeriodDays

Required: False
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

### -EnableDataCompression
Specifies whether the database uses data compression.

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

### -SiteCode
Specifies the site code for a Configuration Manager site.

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

### -SqlServerServiceBrokerPort
Specifies the port that the computer running SQL Server uses as a Service Broker port.

```yaml
Type: Int32
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### 

## NOTES

## RELATED LINKS

[Get-CMDatabaseProperty](Get-CMDatabaseProperty.md)
