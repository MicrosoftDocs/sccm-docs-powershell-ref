---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Set-CMSecurityScope
---

# Set-CMSecurityScope

## SYNOPSIS

Configure a security scope.

## SYNTAX

### SetByValue (Default)
```
Set-CMSecurityScope [-Description <String>] -InputObject <IResultObject> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMSecurityScope [-Description <String>] -Id <String> [-NewName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSecurityScope [-Description <String>] -Name <String> [-NewName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the configuration settings of a security scope. You can only configure custom scopes.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a security scope

The first command gets the security scope object named **Scope1** and stores it in the **$Scope** variable.

The second command changes the name of the security scope to **Admin scope**.

```powershell
$Scope = Get-CMSecurityScope -Name "Scope1"

Set-CMSecurityScope -InputObject $Scope -NewName "Admin scope"
```

## PARAMETERS

### -Description

Specify an optional description for the security scope.

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

### -Id

Specify the ID of a security scope to configure. This value is the `CategoryID` property. Since this cmdlet only works with custom scopes, this value should always start with the site code. (IDs for built-in scopes start with `SMS`.)

```yaml
Type: String
Parameter Sets: SetById
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a security scope object to configure. To get this object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a security scope to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: CategoryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name for the security scope.

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

### System.Object

## NOTES

## RELATED LINKS

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[New-CMSecurityScope](New-CMSecurityScope.md)

[Remove-CMSecurityScope](Remove-CMSecurityScope.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
