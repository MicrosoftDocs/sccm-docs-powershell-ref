---
description: Imports a security role into Configuration Manager.
external help file: AdminUI.PS.Rba.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMSecurityRole
---

# Import-CMSecurityRole

## SYNOPSIS
Imports a security role into Configuration Manager.

## SYNTAX

```
Import-CMSecurityRole -Overwrite <Boolean> -XmlFileName <String> [-NewRoleName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMSecurityRole** cmdlet imports a security role that was exported from another Microsoft System Center Configuration Manager hierarchy.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Import a security role
```
PS XYZ:\>Import-CMSecurityRole -Overwrite $True -XmlFileName "RemoteAdminSecurity.xml"
```

This command imports a security role into Configuration Manager from the XML export file named RemoteAdminSecurity.
The command specifies that the security role that you import overwrites an existing security role with the same name.

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

### -NewRoleName
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

### -Overwrite
Indicates whether the security role that you import overwrites an existing security role with the same name that you specify in the *XmlFileName* parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: OverwrittenExisted

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

### -XmlFileName
Specifies the XML export file that contains the security role definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RolesXml, Path, FileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)


