---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: D7D57FDA-A9BC-40D4-B55B-4190280B2E5F
online version: https://go.microsoft.com/fwlink/?linkid=833920
schema: 2.0.0
---

# Remove-CMBaseline

## SYNOPSIS
Removes configuration baselines.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMBaseline [-Id] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMBaseline [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMBaseline [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBaseline** cmdlet removes one or more configuration baseline items in Microsoft System Center Configuration Manager.
You must remove all references to a configuration baseline before you can remove the configuration baseline.
After you remove a configuration baseline, System Center Configuration Manager removes the configuration baseline from the collection of devices to which you deployed it, and Configuration Manager no longer assesses their compliance with the configuration baseline.

## EXAMPLES

### Example 1: Remove a baseline configuration by using a name
```
PS C:\> Remove-CMBaseline -Name "BLConfigContoso02"
```

This command removes the configuration baseline named BLConfigContoso02.

### Example 2: Remove a baseline configuration by using an ID
```
PS C:\> Remove-CMBaseline -Id "16777366"
```

This command removes the configuration baseline that has the ID 16777366.

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

### -Id
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMBaseline** object.
To obtain a **CMBaseline** object, use the [Get-CMBaseline](./Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
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

[New-CMBaseline](./New-CMBaseline.md)

[Set-CMBaseline](./Set-CMBaseline.md)

[Get-CMBaselineXMLDefinition](./Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](./Get-CMBaselineSummarizationSchedule.md)


