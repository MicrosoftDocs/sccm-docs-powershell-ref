---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Remove-CMSoftwareUpdatePoint
---

# Remove-CMSoftwareUpdatePoint

## SYNOPSIS

Remove a software update point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSoftwareUpdatePoint [-DefaultServerName <String>] [-Force] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareUpdatePoint [-DefaultServerName <String>] [-Force] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a software update point site system role.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a software update point by name

The cmdlet requires both the site code and the name.
Because the command doesn't include the **Force** parameter, this example prompts you for confirmation.

```powershell
Remove-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "UpdateSystem.Western.Contoso.com"
```

### Example 2: Remove a software update point by using a variable

The first command gets a software update point and saves it to the **$CMSUP** variable.

The second command removes the software update point saved in the variable.
This command uses the **Force** parameter, so the cmdlet doesn't prompt you for confirmation.

```powershell
$CMSUP = Get-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "UpdateSystem.Western.Contoso.com"

Remove-CMSoftwareUpdatePoint -InputObject $CMSUP -Force
```

## PARAMETERS

### -DefaultServerName

Specify the FQDN of the default software update point.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DefaultSoftwareUpdatePointServerName

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

### -Force

Add this parameter to run the cmdlet without asking for confirmation.

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

Specify a software update point object to remove. To get this object, use the [Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: SoftwareUpdatePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the three-character code for the site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName

Specify the name of a server that hosts the software update point.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
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

## NOTES

## RELATED LINKS

[Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](Set-CMSoftwareUpdatePoint.md)
