---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: CA239E73-691E-4A34-852A-8417420E68E1
online version: https://go.microsoft.com/fwlink/?linkid=833918
schema: 2.0.0
---

# Copy-CMConfigurationPolicy

## SYNOPSIS
Copies a configuration policy.

## SYNTAX

### SearchByValueMandatory (Default)
```
Copy-CMConfigurationPolicy [-InputObject] <IResultObject> [-NewName] <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Copy-CMConfigurationPolicy [-Id] <Int32> [-NewName] <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Copy-CMConfigurationPolicy [-Name] <String> [-NewName] <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Copy-CMConfigurationPolicy** copies a configuration policy.
A configuration policy can be a client authentication  certificate profile configuration item, a wireless profile configuration item, or others.
See the Alias section for additional policy items that you can use this cmdlet to copy.

## EXAMPLES

### Example 1: Copy a configuration policy by using the pipeline
```
PS C:\> Get-CMConfigurationPolicy -Name "TrustedCACert01" -Fast | Copy-CMConfigurationPolicy -NewName "TrustedCACert01_copy"
```

This command gets the configuration policy object named TrustedCACert01 and uses the pipeline operator to pass the object to **Copy-CMConfiguratinPolicy**, which creates a copy of the policy and names it TrustedCACert01_copy.

### Example 2: Copy a configuration policy by ID
```
PS C:\> Copy-CMConfigurationPolicy -Id 16777454 -NewName "EmailProfile1_copy"
```

This command makes a copy of the configuration policy with the ID of 16777454 and names it EmailProfile1_copy.

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

### -Id
Specifies the CI_ID of a configuration policy.

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
Gets a configuration policy object.
To obtain a configuration policy object, use the Get-CMConfigurationPolicy cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ConfigurationPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a configuration policy.

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

### -NewName
Specifies a name for the copy of the configuration policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

[Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md)

[Remove-CMConfigurationPolicy](Remove-CMConfigurationPolicy.md)


