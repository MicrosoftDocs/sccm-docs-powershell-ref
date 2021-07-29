---
description: Creates a SQL Server settings object in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMSqlServerSetting
---

# New-CMSqlServerSetting

## SYNOPSIS
Creates a SQL Server settings object in Configuration Manager.

## SYNTAX

### NewSettingByExisting (Default)
```
New-CMSqlServerSetting [-InstanceName <String>] -SiteDatabaseName <String>
 [-SqlServerServiceBrokerPort <Int32>] [-UseExistingSqlServerInstance] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewSettingByCopy
```
New-CMSqlServerSetting [-CopySqlServerExpressOnSecondarySite] [-SqlServerServiceBrokerPort <Int32>]
 [-SqlServerServicePort <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSqlServerSetting** cmdlet creates a Microsoft SQL Server settings object in Configuration Manager.
The object specifies settings for the name of the site database and the port number for the SQL Server service and SQL Server Service Broker.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a SQL Server settings object
```
PS XYZ:\> New-CMSqlServerSetting -CopySqlServerExpressOnSecondarySite -SqlServerServiceBrokerPort 4037
```

This command creates a SQL Server settings object that specifies that Configuration Manager copies Microsoft SQL Server Express to a secondary site.
The command specifies that Configuration Manager use port 4037 for the SQL Server Service Broker.

## PARAMETERS

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

### -CopySqlServerExpressOnSecondarySite
Indicates that Microsoft SQL Server Express is copied to a secondary site.

```yaml
Type: SwitchParameter
Parameter Sets: NewSettingByCopy
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

### -InstanceName
Specifies the name of an instance of SQL Server.

```yaml
Type: String
Parameter Sets: NewSettingByExisting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteDatabaseName
Specifies a name of the Configuration Manager site database.

```yaml
Type: String
Parameter Sets: NewSettingByExisting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerServiceBrokerPort
Specifies a port number for the SQL Server Service Broker port.

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

### -SqlServerServicePort
Specifies a port number for the SQL Server service port.

```yaml
Type: Int32
Parameter Sets: NewSettingByCopy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseExistingSqlServerInstance
Indicates that you use the existing instance of SQL Server.

```yaml
Type: SwitchParameter
Parameter Sets: NewSettingByExisting
Aliases:

Required: True
Position: Named
Default value: None
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

### None
## OUTPUTS

### IResultObject#SMS_EmbeddedProperty
### IResultObject[]#SMS_EmbeddedProperty
## NOTES

## RELATED LINKS
