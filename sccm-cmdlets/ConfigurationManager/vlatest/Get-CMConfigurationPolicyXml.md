---
external help file: AdminUI.PS.Dcm-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834283
schema: 2.0.0
ms.assetid: 008C64E0-E41A-4BAB-9C19-7239FB7E262D
---

# Get-CMConfigurationPolicyXml

## SYNOPSIS

## SYNTAX

### ByName (Default)
```
Get-CMConfigurationPolicyXml [[-Name] <String>] [-CategoryInstanceType <String>] [<CommonParameters>]
```

### ById
```
Get-CMConfigurationPolicyXml [-Id] <Int32> [-CategoryInstanceType <String>] [<CommonParameters>]
```

### ByValue
```
Get-CMConfigurationPolicyXml [-InputObject] <IResultObject> [-CategoryInstanceType <String>]
 [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -CategoryInstanceType


```yaml
Type: String
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

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


