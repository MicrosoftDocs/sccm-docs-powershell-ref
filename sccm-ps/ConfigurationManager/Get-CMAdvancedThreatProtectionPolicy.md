---
external help file: AdminUI.PS.Dcm-help.xml
online version: 
schema: 2.0.0
---

# Get-CMAdvancedThreatProtectionPolicy

## SYNOPSIS
Gets an advanced threat protection policy

## SYNTAX

### ByValue (Default)
```
Get-CMAdvancedThreatProtectionPolicy [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMAdvancedThreatProtectionPolicy [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMAdvancedThreatProtectionPolicy [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1
```
PS XYZ:\>  
```

 

## PARAMETERS

### -Fast
 

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
 

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

