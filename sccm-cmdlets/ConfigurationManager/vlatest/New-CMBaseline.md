---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834266
schema: 2.0.0
ms.assetid: 10D58015-8146-4A5F-8996-31BF2BD06DF9
---

# New-CMBaseline

## SYNOPSIS
Creates a Configuration Manager baseline.

## SYNTAX

```
New-CMBaseline -Name <String> [-Description <String>] [-Category <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBaseline** cmdlet creates a Microsoft System Center Configuration Manager baseline.
A baseline is a collection of configuration items that System Center Configuration Manager uses to evaluate whether a computer complies with software requirements.
After you create a baseline, you can deploy it to a collection so that devices in that collection download the configuration baseline and assess compliance with it.

## EXAMPLES

### Example 1: Create a configuration baseline
```
PS C:\> New-CMBaseline -Name "Accounting Department baseline" -Description "Compliance standards for Accounting computers."
```

This command creates a baseline for compliance named Accounting Department baseline.
The command specifies a description for the baseline.

## PARAMETERS

### -Category
Specifies an array of categories to which the baseline configuration belongs.
Valid values are: 

- Client
- IT Infrastructure
- Line of Business
- Server

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceNames
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

### -Description
Specifies a description for the baseline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription
Required: False
Position: Named
Default value: None
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

### -Name
Specifies a name for the configuration baseline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMBaseline](./Disable-CMBaseline.md)

[Enable-CMBaseline](./Enable-CMBaseline.md)

[Export-CMBaseline](./Export-CMBaseline.md)

[Get-CMBaseline](./Get-CMBaseline.md)

[Import-CMBaseline](./Import-CMBaseline.md)

[Remove-CMBaseline](./Remove-CMBaseline.md)

[Set-CMBaseline](./Set-CMBaseline.md)


