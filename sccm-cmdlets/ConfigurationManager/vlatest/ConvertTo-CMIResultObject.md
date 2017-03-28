---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833914
schema: 2.0.0
ms.assetid: 5F39BFCE-FF04-4DB0-BF85-4C495CAE7A23
---

# ConvertTo-CMIResultObject

## SYNOPSIS
Converts a **ManagementBaseObject** to an **IResultObject**.

## SYNTAX

```
ConvertTo-CMIResultObject -InputObject <ManagementBaseObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Convertto-CMIResultObject** cmdlet converts a **ManagementBaseObject** to an **IResultObject**.

## EXAMPLES

### Example 1: Convert a ManagementBaseObject to an IResultObject by passing a WMI object through the pipeline
```
PS ABC:\> $WmiObject = Get-WmiObject -Query "SELECT * FROM SMS_Site" -Namespace "root\sms\site_PS1"
PS ABC:\> $WmiObject | ConvertTo-CMIResultObject
```

The first command gets the site object with the code of PS1 and stores the object in the $WmiObject variable.

The second command uses the pipeline operator to pass the site object stored in $WmiObject to **ConvertTo-CMIResultObject**, which converts the site object to an **IResultObject**.

### Example 2: Convert a ManagementBaseObject to an IResultObject by getting a WMI object
```
PS ABC:\> $WmiObject = Get-WmiObject -Query "SELECT * FROM SMS_Site" -Namespace "root\sms\site_PS1"
PS ABC:\> ConvertTo-CMIResultObject -InputObject $WmiObject
```

The first command gets the site object with the code of PS1 and stores the object in the $WmiObject variable.

The second command converts the site object stored in $WmiObject to an **IResultObject**.

## PARAMETERS

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

### -InputObject
Specifies the **ManagementBaseObject** to convert to an **IResultObject**.

```yaml
Type: ManagementBaseObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[ConvertFrom-CMIResultObject](./ConvertFrom-CMIResultObject.md)
