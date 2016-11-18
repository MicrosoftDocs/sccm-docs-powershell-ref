---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 73C8ACBF-E83D-4AC9-AC89-7780D5950FE0
---

# New-CMSecurityScope

## SYNOPSIS
Creates a security scope.

## SYNTAX

```
New-CMSecurityScope -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSecurityScope** cmdlet creates a security scope.
Security scopes provide administrative users with access to securable objects.

## EXAMPLES

### Example 1: Create a security scope
```
PS C:\>New-CMSecurityScope -Name "testSecope" -Description "Security Scope"
```

This command creates a security scope named testScope.

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

### -Description
Specifies a description for the security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryDescription

Required: False
Position: Named
Default value: None
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

### -Name
Specifies a name for the security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryName

Required: True
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

[Get-CMSecurityScope](./Get-CMSecurityScope.md)

[Set-CMSecurityScope](./Set-CMSecurityScope.md)

[Remove-CMSecurityScope](./Remove-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](./Remove-CMSecurityScopeFromAdministrativeUser.md)


