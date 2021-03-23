---
description: Gets a EULA or SLT for a software update in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareUpdateLicense
---

# Get-CMSoftwareUpdateLicense

## SYNOPSIS
Gets a EULA or SLT for a software update in Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateLicense [-EulaAcceptance <EulaAcceptance>] [-Name <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMSoftwareUpdateLicense [-EulaAcceptance <EulaAcceptance>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateLicense** cmdlet gets an End User License Agreement (EULA) or Software License Terms (SLT) for a software update in Configuration Manager.
You can specify a software update by ID or by name or use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet to obtain one.
If you specify an ID or name, you can further specify a security scope membership.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a EULA or SLT for a software update
```
PS XYZ:\> Get-CMSoftwareUpdateLicense -Name "UpdatePkg01" -SecuredScopeNames "SecScope02"
```

This command gets the EULA or SLT for a software update named UpdatePkg01 for the security scope named SecScope02.

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

### -EulaAcceptance
```yaml
Type: EulaAcceptance
Parameter Sets: (All)
Aliases:
Accepted values: Declined, Accepted, Unknown

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
Specifies a software update object.
To obtain a software update object, use the **Get-CMSoftwareUpdate** cmdlet.

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
Specifies an array of names of software updates.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.String[]

### System.String

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)
