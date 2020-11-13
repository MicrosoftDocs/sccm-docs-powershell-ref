---
description: Exports a security role to an XML file.
external help file: AdminUI.PS.Rba.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Export-CMSecurityRole
---

# Export-CMSecurityRole

## SYNOPSIS
Exports a security role to an XML file.

## SYNTAX

### ByValue (Default)
```
Export-CMSecurityRole -InputObject <IResultObject> -Path <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Export-CMSecurityRole -Path <String> -RoleId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Export-CMSecurityRole -Path <String> -RoleName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMSecurityRole** cmdlet exports a security role configuration from Configuration Manager to an XML file.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Export a security role
```
PS XYZ:\>Export-CMSecurityRole -Path "\\Contoso01\Export\Sec_Roles\Security_Manager" -RoleId "SMS000CR"
```

This command exports the security role named SMS000CR to the file named Security_Manager.

## PARAMETERS

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Specifies the path to which you export the XML file for the security role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExportFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleId
Specifies the ID of a role.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
```yaml
Type: String
Parameter Sets: ByName
Aliases:

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)


