---
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMAzureService

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByName (Default)
```
Get-CMAzureService [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAzureService -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
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

### -Id
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SearchByName
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

### None

## OUTPUTS

### IResultObject#SMS_Azure_CloudService

## NOTES

## RELATED LINKS
