---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834073
schema: 2.0.0
ms.assetid: AB20D6C3-3817-400F-B098-371536B4513C
---

# Get-CMAlert

## SYNOPSIS
Gets Configuration Manager alerts.

## SYNTAX

### SearchByName (Default)
```
Get-CMAlert [[-Name] <String>] [-TypeInstanceId <String>] [-TypeId <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAlert [-Id] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAlert** cmdlet gets one or more Microsoft System Center Configuration Manager alerts.
You can get a specific alert by specifying the name or ID of the alert.

## EXAMPLES

### Example 1: Get all alerts
```
PS C:\>Get-CMAlert
```

This command gets all alerts that System Center Configuration Manager manages.

### Example 2: Get alerts by using name
```
PS C:\>Get-CMAlert -Name "D*"
```

This command gets all alerts that have a name that begins with the letter D.

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

### -Id
Specifies an alert ID.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an alert name.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeId


```yaml
Type: Int32
Parameter Sets: SearchByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeInstanceId


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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-CMAlert](./Enable-CMAlert.md)

[Remove-CMAlert](./Remove-CMAlert.md)

[Set-CMAlert](./Set-CMAlert.md)

[Suspend-CMAlert](./Suspend-CMAlert.md)

[Disable-CMAlert](./Disable-CMAlert.md)


