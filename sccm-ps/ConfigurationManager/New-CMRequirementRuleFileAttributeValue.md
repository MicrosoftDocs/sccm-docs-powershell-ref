---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMRequirementRuleFileAttributeValue

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMRequirementRuleFileAttributeValue [-FileArchive <AttributeVerificationOption>]
 [-FileCompressed <AttributeVerificationOption>] [-FileEncrypted <AttributeVerificationOption>]
 [-FileHidden <AttributeVerificationOption>] [-FileReadOnly <AttributeVerificationOption>]
 [-FileSystem <AttributeVerificationOption>] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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

### -FileArchive
{{ Fill FileArchive Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileCompressed
{{ Fill FileCompressed Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileEncrypted
{{ Fill FileEncrypted Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileHidden
{{ Fill FileHidden Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileReadOnly
{{ Fill FileReadOnly Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
{{ Fill FileSystem Description }}

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: GlobalCondition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
