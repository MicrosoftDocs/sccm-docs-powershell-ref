---
description: Removes an enrollment point.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMEnrollmentPoint
---

# Remove-CMEnrollmentPoint

## SYNOPSIS
Removes an enrollment point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMEnrollmentPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMEnrollmentPoint [-Force] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMEnrollmentPoint** cmdlet removes an enrollment point in Configuration Manager.
An enrollment point is a site system role that uses public key infrastructure (PKI) certificates to complete mobile device enrollment and to provision Intel AMT-based computers.
After you remove an enrollment point, client computers and devices must use a different enrollment point.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove an enrollment point
```
PS XYZ:\> Remove-CMEnrollmentPoint -SiteSystemServerName "SiteServer01.Contoso.com" -SiteCode "CM1"
```

This command removes an enrollment point.

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
Specifies the input to this cmdlet.
You can use the Get-CMEnrollmentPoint cmdlet to get an input object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: EnrollmentPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

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
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

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

### 

## NOTES

## RELATED LINKS

[Add-CMEnrollmentPoint](Add-CMEnrollmentPoint.md)

[Get-CMEnrollmentPoint](Get-CMEnrollmentPoint.md)

[Set-CMEnrollmentPoint](Set-CMEnrollmentPoint.md)


