---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834007
schema: 2.0.0
ms.assetid: C7C14E05-2CB8-4D9E-92A5-81838CF88799
---

# Remove-CMConfigurationPolicy

## SYNOPSIS
Removes a configuration policy.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMConfigurationPolicy [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Remove-CMConfigurationPolicy [-Id] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMConfigurationPolicy [-Name] <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMConfigurationPolicy** cmdlet removes a configuration policy.
A configuration policy can be an email profile, a firewall policy, or others.
See the Alias section for additional policy types that you can use this cmdlet to remove.

## EXAMPLES

### Example 1: Remove a configuration policy by ID
```
PS C:\> Remove-CMConfigurationPolicy -ID 16777454 -Force
```

This command removes the configuration policy with the CI_ID of 16777454, without prompting the user for confirmation.

### Example 2: Remove a configuration policy by name
```
PS C:\> Get-CMcertificateProfilePfx -Name "CertProf1" | Remove-CMConfigurationPolicy
```

This command gets the PFX certificate profile object named CertProf01 and uses the pipeline operator to pass the object to **Remove-CMConfigurationPolicy** which removes the certificate profile.

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
To obtain a configuration policy object, use the Get-CMConfigurationPolicy cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration policies.

```yaml
Type: String[]
Parameter Sets: SearchByName
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

[Copy-CMConfigurationPolicy](./Copy-CMConfigurationPolicy.md)

[Get-CMConfigurationPolicy](./Get-CMConfigurationPolicy.md)


