---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Export-CMSecurityRole
---

# Export-CMSecurityRole

## SYNOPSIS

Export a security role to an XML file.

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

Use this cmdlet to export the configuration of a custom security role from the site to an XML file. You can't export built-in roles. For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Export a custom security role

This command exports the custom security role named **XYZ00001** to the file named **Security_Manager.xml**.

```powershell
Export-CMSecurityRole -Path "\\Contoso01\Export\Sec_Roles\Security_Manager.xml" -RoleId "XYZ00001"
```

## PARAMETERS

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

Specify a security role object to export. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

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

Specify the path of the XML file to export the security role. It can be a local or network path. Include the `.xml` file extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, ExportFilePath, XmlFileName, RolesXml

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleId

Specify the ID of the security role to export. This value is the `RoleID` property. Since this cmdlet only works with custom roles, this value should always start with the site code. (IDs for built-in roles start with `SMS`.)

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

Specify the name of the security role to export.

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

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
