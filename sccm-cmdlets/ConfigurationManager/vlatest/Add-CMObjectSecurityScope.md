---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 86912EF1-D554-4D99-AB38-FADC0EC1F686
---

# Add-CMObjectSecurityScope

## SYNOPSIS
Adds a security scope to an object.

## SYNTAX

### ByValue (Default)
```
Add-CMObjectSecurityScope -InputObject <IResultObject[]> [-Scope] <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Add-CMObjectSecurityScope -Id <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMObjectSecurityScope -InputObject <IResultObject[]> [-Name] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMObjectSecurityScope** cmdlet adds security scope to a Microsoft System Center Configuration Manager object.

## EXAMPLES

### Example 1: Add a security scope to application objects by using the pipeline
```
PS C:\>$Scope = New-CMSecurityScope -Name "Scope1" -Description "Security scope 1"
PS C:\> Get-CMApplication -Name "Application*" | Add-CMObjectSecurityScope -Scope $Scope
```

The first command creates a security scope object named Scope1 and stores the object in the $Scope variable.

The second command gets all application objects that have a name beginning with "Application" and uses the pipeline operator to pass the objects to **Add-CMObjectSecurityScope**.
**Add-CMObjectSecurityScope** adds the security scope stored in $Scope to each application object.

### Example 2: Add a security scope to application objects
```
PS C:\>Add-CMObjectSecurityScope -Name "Scope1" -InputObject (Get-CMApplication -Name "Application*")
```

This command gets all application objects that have a name beginning with "Application" and then adds the security scope named Scope1 to each application object.

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
Parameter Sets: ById
Aliases: SecurityScopeId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an array of objects to which you want to assign a security scope.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope that this cmdlet adds.
A security scope name can be Default or the name of a custom security scope.

```yaml
Type: String
Parameter Sets: ByName
Aliases: SecurityScopeName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Specifies an array of security scopes.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: SecurityScope, SecuredCategory, Scopes, SecurityScopes, SecuredCategories

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

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMObjectSecurityScope](./Get-CMObjectSecurityScope.md)

[New-CMSecurityScope](./New-CMSecurityScope.md)

[Remove-CMObjectSecurityScope](./Remove-CMObjectSecurityScope.md)

[Set-CMObjectSecurityScope](./Set-CMObjectSecurityScope.md)


