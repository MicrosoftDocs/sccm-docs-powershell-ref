---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Set-CMObjectSecurityScope
---

# Set-CMObjectSecurityScope

## SYNOPSIS

Add or remove security scopes for Configuration Manager objects. This cmdlet is deprecated.

## SYNTAX

```
Set-CMObjectSecurityScope -Action <SecurityScopeActionType> -InputObject <IResultObject[]> -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMObjectSecurityScope** cmdlet adds and removes security scopes for Configuration Manager objects.

This cmdlet has been deprecated and may be removed in a future release.
Use [Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md) and [Remove-CMObjectSecurityScope](Remove-CMObjectSecurityScope.md) to add and remove security scopes from Configuration Manager objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a security scope to application objects by using the pipeline
```
PS XYZ:\> Get-CMApplication -Name "Application*" | Set-CMObjectSecurityScope -Action AddMembership -Name "Scope1"
```

This command gets all application objects that have a name beginning with Application and uses the pipeline operator to pass the objects to **Set-CMObjectSecurityScope**.
**Set-CMObjectSecurityScope** adds the security scope named Scope1 to each application object.

### Example 2: Add a security scope to application objects
```
PS XYZ:\> Set-CMObjectSecurityScope -InputObject (Get-CMApplication -Name "Application*") -Action AddMembership -Name "Scope1"
```

This command gets all application objects that have a name beginning with Application and adds the security scope named Scope1 to each application object.

## PARAMETERS

### -Action
Specifies the action that this cmdlet takes on the security scope.
Valid values are:

- AddMembership
- RemoveMembership

```yaml
Type: SecurityScopeActionType
Parameter Sets: (All)
Aliases: SecurityScopeAction
Accepted values: AddMembership, RemoveMembership

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

### -InputObject
Specifies an array of Configuration Manager objects associated with a security scope.

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
Specifies a name of a security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecurityScopeName

Required: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md)

[Get-CMObjectSecurityScope](Get-CMObjectSecurityScope.md)

[Remove-CMObjectSecurityScope](Remove-CMObjectSecurityScope.md)
