---
description: Gets a configuration policy.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMConfigurationPolicy
---

# Get-CMConfigurationPolicy

## SYNOPSIS
Gets a configuration policy.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationPolicy [-AsXml] [-CategoryInstanceType <String[]>] [-Fast] [[-Name] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMConfigurationPolicy [-AsXml] [-CategoryInstanceType <String[]>] [-Fast] [-Id] <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMConfigurationPolicy [-AsXml] [-CategoryInstanceType <String[]>] [-Fast] [[-InputObject] <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConfigurationPolicy** cmdlet gets a configuration policy.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a configuration policy by name
```
PS XYZ:\> Get-CMConfigurationPolicy -Name "TrustedCACert01" -AsXml
```

This command gets the configuration policy named TrustedCACert01 and displays the output in XML format.

### Example 2: Get a configuration policy by ID
```
PS XYZ:\> Get-CMConfigurationPolicy -Id 16777454 -Fast
```

This command gets the configuration policy with the ID of 16777454 and does not display lazy properties.

## PARAMETERS

### -AsXml
Specifies that the configuration policy is returned in XML format.

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

### -CategoryInstanceType
Specifies an array of category instance types.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CategoryInstanceTypes

Required: False
Position: Named
Default value: None
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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -Id
Specifies the CI__ID of a configuration policy.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a configuration policy object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a configuration policy.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_ConfigurationPolicy

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Copy-CMConfigurationPolicy](Copy-CMConfigurationPolicy.md)

[Remove-CMConfigurationPolicy](Remove-CMConfigurationPolicy.md)


