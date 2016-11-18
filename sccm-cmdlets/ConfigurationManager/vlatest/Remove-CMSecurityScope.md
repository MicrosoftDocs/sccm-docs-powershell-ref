---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 5A75BC8C-977B-4AAF-BA2E-9A5164628A62
---

# Remove-CMSecurityScope

## SYNOPSIS
Removes a security scope.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSecurityScope -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSecurityScope -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMSecurityScope -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityScope** cmdlet removes a security scope from Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Remove a security scope in a variable
```
PS C:\>$Scope = Get-CMSecurityScope -Name "Scope"
PS C:\> Remove-CMSecurityScope -InputObject $Scope -Force
```

The first command gets the security scope object named Scope and stores the object in the $Scope variable.

The second command removes the security scope stored in $Scope.
By specifying the *Force* parameter, the user is not prompted for confirmation prior to the security scope being removed.

### Example 2: Remove a security scope using the pipeline
```
PS C:\>Get-CMSecurityScope -Name "Scope" | Remove-CMSecurityScope -Force
```

This command gets the security scope object named Scope and uses the pipeline operator to pass the object to **Remove-CMSecurityScope**, which removes the security scope.
By specifying the *Force* parameter, the user is not prompted for confirmation prior to the security scope being removed.

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

### -Id
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSecurityScope** object.
To obtain a **CMSecurityScope** object, use the Get-CMSecurityScope cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of security scope.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[New-CMSecurityScope](./New-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](./Remove-CMSecurityScopeFromAdministrativeUser.md)

[Set-CMSecurityScope](./Set-CMSecurityScope.md)


