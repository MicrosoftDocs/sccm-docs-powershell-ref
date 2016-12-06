---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833869
schema: 2.0.0
ms.assetid: E1819266-4602-4752-A526-BA365AFA70C4
---

# Remove-CMActiveDirectoryForest

## SYNOPSIS
Removes an Active Directory forest object from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMActiveDirectoryForest [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByFQDNMandatory
```
Remove-CMActiveDirectoryForest [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMActiveDirectoryForest** cmdlet removes an Active Directory forest object from Microsoft System Center Configuration Manager.
You can specify an Active Directory forest by using the ID property or the fully qualified domain name (FQDN), or you can supply the Active Directory forest itself.

## EXAMPLES

### Example 1: Remove an Active Directory forest object by ID
```
PS C:\>Remove-CMActiveDirectoryForest -Id "16777217"
```

This command removes an Active Directory forest object that has the ID 16777217.

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies an Active Directory forest object in Configuration Manager.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: SearchByFQDNMandatory
Aliases: ForestFqdn
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

[New-CMActiveDirectoryForest](./New-CMActiveDirectoryForest.md)

[Get-CMActiveDirectoryForest](./Get-CMActiveDirectoryForest.md)

[Set-CMActiveDirectoryForest](./Set-CMActiveDirectoryForest.md)


