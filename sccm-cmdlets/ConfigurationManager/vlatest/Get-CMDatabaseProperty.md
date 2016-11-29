---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834295
schema: 2.0.0
ms.assetid: 04AC8F78-1E8D-4FBC-B87E-732B52D09F9E
---

# Get-CMDatabaseProperty

## SYNOPSIS
Gets an object that represents a Configuration Manager database.

## SYNTAX

```
Get-CMDatabaseProperty [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDatabaseProperty** cmdlet gets an object that represents a Microsoft System Center Configuration Manager database.
Use the site code for a site to specify a database.

When this cmdlet returns a database object in the console, it displays current settings for data compression, Broker port for the computer that runs Microsoft SQL Server, and the length of time that the database keeps data.
You can use the Set-CMDatabaseProperty cmdlet to change these values.

## EXAMPLES

### Example 1: Get a database property
```
PS C:\>Get-CMDatabaseProperty -SiteCode "CM2"
Key                                     Value
---                                     -----
SQL Server Service Broker Port          80 
Retention Period                        10 
IsCompression                           0
```

This command gets the database property for the site that has the site code CM2.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMDatabaseProperty](./Set-CMDatabaseProperty.md)


